# Passage by 1Password (passage-1password)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Passage by 1Password is a passwordless authentication platform that lets developers add passkeys (WebAuthn), magic links, and biometric login to their apps. It exposes a REST Management API at https://api.passage.id/v1 for server-side user administration (CRUD, devices, tokens) and magic link creation, alongside frontend Auth/WebAuthn flows. Note - 1Password has announced that the Passage product is being retired on 2026-01-16; this catalog documents the API as published and is distinct from the separate 1Password secrets-manager catalog.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/passage-1password/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/passage-1password/refs/heads/main/apis.yml)

> This is the **Passage** passwordless / passkey product by 1Password (passage.1password.com, api.passage.id). It is intentionally kept separate from the `1password` catalog repo, which covers the 1Password secrets-manager surface (Connect Server, Events, SCIM).

## Tags

- Authentication
- Passkeys
- WebAuthn
- Passwordless
- Identity
- Magic Links

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Passage Management API

Server-side REST API authenticated with a Bearer API key for administering a Passage app's users - paginated list, create, get, update, delete, activate, deactivate, list/delete WebAuthn devices, and revoke refresh tokens.

- **Human URL:** [https://docs.passage.id/api-docs/management-api](https://docs.passage.id/api-docs/management-api)
- **Base URL:** `https://api.passage.id/v1`

#### Tags

- Management
- Apps
- Users

#### Properties

- [Documentation](https://docs.passage.id/api-docs/management-api)
- [API Reference](https://docs.passage.id/api-docs/management-api)
- [OpenAPI](openapi/passage-1password-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/passage-1password.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/passage-1password.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Passage Users API

User lifecycle operations under `/apps/{app_id}/users` - paginated and filterable listing, create by email/phone with user_metadata, get, update, delete, activate/deactivate, list and delete registered WebAuthn devices, and revoke a user's refresh tokens.

- **Human URL:** [https://docs.passage.id/api-docs/management-api](https://docs.passage.id/api-docs/management-api)
- **Base URL:** `https://api.passage.id/v1`

#### Tags

- Users
- CRUD
- Devices

#### Properties

- [Documentation](https://docs.passage.id/api-docs/management-api)
- [OpenAPI](openapi/passage-1password-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/passage-1password.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/passage-1password.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Passage Magic Links API

Creates embedded or sent magic links via `POST /apps/{app_id}/magic-links` for login or identifier verification, with email/phone channel, language, TTL, redirect URL, and optional auto-send. Creates the user if they do not yet exist.

- **Human URL:** [https://docs.passage.id/complete/magic-links](https://docs.passage.id/complete/magic-links)
- **Base URL:** `https://api.passage.id/v1`

#### Tags

- Magic Links
- Passwordless
- Email

#### Properties

- [Documentation](https://docs.passage.id/complete/magic-links)
- [OpenAPI](openapi/passage-1password-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/passage-1password.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/passage-1password.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Passage Authentication API

Frontend passwordless authentication flows - passkey (WebAuthn) registration and login, magic link redemption, and JWT issuance. These flows are driven by the Passage frontend SDKs / Elements and validated server-side against the app's JWKS; user state is reflected through the Management API surface.

- **Human URL:** [https://docs.passage.id/home](https://docs.passage.id/home)
- **Base URL:** `https://api.passage.id/v1`

#### Tags

- Authentication
- Passkeys
- WebAuthn

#### Properties

- [Documentation](https://docs.passage.id/home)
- [OpenAPI](openapi/passage-1password-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/passageidentity)
- [LinkedIn](https://www.linkedin.com/company/1password)
- [Website](https://passage.1password.com)
- [Documentation](https://docs.passage.id/home)
- [Plans](plans/passage-1password-plans-pricing.yml)
- [Rate Limits](rate-limits/passage-1password-rate-limits.yml)
- [Fin Ops](finops/passage-1password-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
