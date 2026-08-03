# Algbra (algbra)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
