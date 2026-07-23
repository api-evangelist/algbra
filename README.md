# Algbra (algbra)

Algbra is a UK values-based, sustainability-focused fintech operated by Algbra FS UK Limited (company number 12629086), an electronic money institution authorised by the Financial Conduct Authority under the Electronic Money Regulations 2011 (FRN 952360); its parent, Algbra Group Limited, is a certified B Corporation. As a non-CMA9 challenger provider it offers ethical multi-currency accounts, cards, savings and Banking-as-a-Service infrastructure, and through the Algbra Labs developer platform it exposes a first-party Partner Banking (BaaS) API alongside a UK Open Banking dedicated interface conformant to the OBIE Read/Write Standard v3.1.8 (delivered via the Tell Money / Tell Connect platform).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/algbra/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/algbra/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Open Banking
- PSD2
- OBIE
- United Kingdom
- Payments
- Account Information
- Fintech
- Ethical Finance
- Banking as a Service

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

### Algbra Account and Transaction Information API (AIS)

Algbra's UK Open Banking Account & Transaction Information (AIS) dedicated interface, conformant to the OBIE Read/Write Standard v3.1, enabling authorised AISP Third Party Providers to create account-access consents and read accounts, balances, beneficiaries and transactions with the customer's consent. Secured with FAPI OAuth2/OIDC, mTLS and PSD2 SCA.

- **Human URL:** [https://developer.algbralabs.com/open-banking-uk/introduction](https://developer.algbralabs.com/open-banking-uk/introduction)
- **Base URL:** `https://secure.tell.systems/algbra/open-banking/v3.1/aisp`

#### Tags

- Account Information
- Open Banking
- AIS

#### Properties

- [OpenAPI](openapi/algbra-account-transaction-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.algbralabs.com/open-banking-uk/introduction)
- [API Reference](https://developer.algbralabs.com/open-banking-uk/api-reference)

### Algbra Payment Initiation API (PIS)

Algbra's UK Open Banking Payment Initiation (PIS) dedicated interface under the OBIE Read/Write Standard v3.1.8, allowing authorised PISP Third Party Providers to initiate payments on a customer's behalf (scope `payments`).

- **Human URL:** [https://developer.algbralabs.com/open-banking-uk/introduction](https://developer.algbralabs.com/open-banking-uk/introduction)
- **Base URL:** `https://secure.tell.systems/algbra/open-banking/v3.1/pisp`

#### Tags

- Payments
- Open Banking
- PIS

#### Properties

- [Documentation](https://developer.algbralabs.com/open-banking-uk/introduction)
- [API Reference](https://openbankinguk.github.io/read-write-api-site3/v3.1.8/profiles/)

### Algbra Confirmation of Funds API (CBPII)

Algbra's UK Open Banking Confirmation of Funds (CBPII) dedicated interface under the OBIE Read/Write Standard v3.1.8, allowing authorised CBPII Third Party Providers to confirm the availability of funds (scope `fundsconfirmations`).

- **Human URL:** [https://developer.algbralabs.com/open-banking-uk/introduction](https://developer.algbralabs.com/open-banking-uk/introduction)
- **Base URL:** `https://secure.tell.systems/algbra/open-banking/v3.1/cbpii`

#### Tags

- Confirmation of Funds
- Open Banking
- CBPII

#### Properties

- [Documentation](https://developer.algbralabs.com/open-banking-uk/introduction)
- [API Reference](https://openbankinguk.github.io/read-write-api-site3/v3.1.8/profiles/)

### Algbra Partner Banking API

Algbra Labs' first-party Partner Banking (Banking-as-a-Service) API for B2B partners, covering customer onboarding and compliance checks, primary and virtual accounts, card issuing, internal/inbound/outbound and automated payments, counterparty validation, transactions, activity feeds, investments and webhooks. Secured with API keys, mTLS and payload signing over IP-whitelisted hosts.

- **Human URL:** [https://developer.algbralabs.com/partner-banking/introduction](https://developer.algbralabs.com/partner-banking/introduction)
- **Base URL:** `https://horizon-link.algbralabs.com`

#### Tags

- Banking as a Service
- Payments
- Accounts

#### Properties

- [Documentation](https://developer.algbralabs.com/partner-banking/introduction)
- [Getting Started](https://developer.algbralabs.com/partner-banking/getting-started)
- [Authentication](https://developer.algbralabs.com/partner-banking/getting-started/authentication)
- [API Hosts](https://developer.algbralabs.com/partner-banking/getting-started/api-hosts)
- [Webhooks](https://developer.algbralabs.com/partner-banking/concepts/webhooks)

## Common Properties

- [Website](https://www.algbra.com/)
- [Developer Portal](https://developer.algbralabs.com/home)
- [Documentation](https://developer.algbralabs.com/open-banking-uk/introduction)
- [Sign Up / Partner Onboarding](https://developer.algbralabs.com/partner-banking/getting-started/partner-onboarding)
- [Blog](https://www.algbra.com/news/category/blog/)
- [Pricing (Fees and Charges)](https://www.algbra.com/fees-and-charges/)
- [Terms of Service](https://www.algbra.com/terms-and-conditions/)
- [Privacy Policy](https://www.algbra.com/privacy-policy/)
- [Support](https://www.algbra.com/help/)
- [Vulnerability Disclosure (Responsible Disclosure)](https://www.algbra.com/responsible-disclosure/)
- [LinkedIn](https://algbra.com/socials/linkedin)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
