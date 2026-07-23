---
name: Access Algbra account & transaction data (OBIE AIS)
description: >-
  Operating instructions for an AISP agent to set up an account-access consent and
  read a customer's accounts, balances, beneficiaries and transactions through
  Algbra's UK Open Banking (OBIE) dedicated interface, delivered via Tell Money.
api: openapi/algbra-account-transaction-api-openapi.yml
operations:
  - CreateAccountAccessConsents
  - GetAccountAccessConsentsConsentId
  - GetAccounts
  - GetAccountsAccountId
  - GetAccountsAccountIdBalances
  - GetAccountsAccountIdBeneficiaries
  - GetAccountsAccountIdTransactions
  - DeleteAccountAccessConsentsConsentId
---

# Access Algbra account & transaction data (OBIE AIS)

Base path: `/algbra/open-banking/v3.1/aisp` on `https://secure.tell.systems`.
You must be an FCA-authorised AISP with OBIE OBWAC/OBSEAL eIDAS certificates and a
registered client (OBIE DCR v3.2). The interface is FAPI + mutual-TLS + PSD2 SCA.

## Prerequisites
- Obtain a client-credentials token (`TPPOAuth2Security`, scope `accounts`) from
  `https://secure.tell.systems/algbra/auth/oidc/token` over mutual-TLS.
- Send FAPI headers on every call: `x-fapi-financial-id`, `x-fapi-interaction-id`
  (echo for correlation), `x-fapi-customer-ip-address`, `Authorization: Bearer`.

## Steps
1. **Create a consent** — `CreateAccountAccessConsents` (`POST /account-access-consents`)
   with an `OBReadConsent1` body listing the `Permissions` you need
   (e.g. `ReadAccountsDetail`, `ReadBalances`, `ReadTransactionsDetail`,
   `ReadBeneficiariesDetail`). Returns a `ConsentId` in `AwaitingAuthorisation`.
2. **Authorise (PSU/SCA)** — redirect the customer through the OIDC authorization
   endpoint (`PSUOAuth2Security`, `response_type code id_token`) so they complete
   Strong Customer Authentication; exchange the code for an access token bound to
   the `ConsentId`.
3. **Confirm consent status** — `GetAccountAccessConsentsConsentId`
   (`GET /account-access-consents/{ConsentId}`) and verify `Status: Authorised`.
4. **List accounts** — `GetAccounts` (`GET /accounts`); take each `AccountId`.
5. **Read details** — per account: `GetAccountsAccountId`,
   `GetAccountsAccountIdBalances`, `GetAccountsAccountIdBeneficiaries`,
   `GetAccountsAccountIdTransactions`. Page with the OBIE `Links.Next` URL until absent.
6. **Revoke when done** — `DeleteAccountAccessConsentsConsentId`
   (`DELETE /account-access-consents/{ConsentId}`).

## Rules
- Errors use the OBIE `OBErrorResponse1` envelope (`Code`, `Id`, `Message`,
  `Errors[].ErrorCode` = `UK.OBIE.*`) — not RFC 9457. See `errors/algbra-problem-types.yml`.
- Paginate via `Links` (Self/First/Prev/Next/Last) + `Meta.TotalPages`; do not
  guess offsets. See `conventions/algbra-conventions.yml`.
- Respect `429 Too Many Requests`; back off and retry with the same `x-fapi-interaction-id`.
- Only request the minimum `Permissions` the use case needs (PSD2 data minimisation).
