# Passage by 1Password (passage-1password)

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
