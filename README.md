# Toyota (toyota)

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

Toyota Motor Corporation is a Japanese multinational automotive manufacturer that designs, manufactures, and sells vehicles, including cars, trucks, and buses. Founded in 1937, Toyota has become one of the largest automakers in the world, known for its reliability, innovation, and commitment to sustainability. Toyota's developer platform (developer.eig.toyota.com) provides APIs for vehicle lifecycle management, telematics and connected services, dealer data, and fleet management for business partners, dealers, fleet operators, and developers building mobility applications. Toyota's product lineup includes hybrids like the Prius, trucks like the Tacoma, and EVs including the bZ4X.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/toyota/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/toyota/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Automobiles
- Cars
- Vehicles
- Connected Car
- Telematics
- Fleet Management
- Electric Vehicles

## Timestamps

- **Created:** 2025-02-25
- **Modified:** 2026-05-19

## APIs

### Toyota Vehicle API

Toyota Vehicle API provides lifecycle information for vehicles from initial order through retail sale. Enables dealers, fleet managers, and authorized business partners to access vehicle inventory, order status, and vehicle configuration data for Toyota North America vehicles.

- **Human URL:** [https://developer.eig.toyota.com/apis/vehicle](https://developer.eig.toyota.com/apis/vehicle)

#### Tags

- Automotive
- Vehicles
- Connected Car
- Vehicle Lifecycle
- Dealer

#### Properties

- [Documentation](https://developer.eig.toyota.com/apis/vehicle)
- [OpenAPI](openapi/toyota-vehicle-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Toyota Telematics API

Toyota Telematics API provides details related to connected services, satellite radio subscriptions, and vehicle health data for enrolled vehicles based on Unit ID or VIN. Supports fleet management, rental car operations, and telematics insurance use cases.

- **Human URL:** [https://developer.eig.toyota.com/apis/telematics](https://developer.eig.toyota.com/apis/telematics)

#### Tags

- Automotive
- Telematics
- Connected Car
- Fleet Management
- Vehicle Health

#### Properties

- [Documentation](https://developer.eig.toyota.com/apis/telematics)
- [OpenAPI](openapi/toyota-telematics-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/toyota-telematics.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/toyota-telematics.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Toyota Connected Services API

Toyota Connected Services API enables authorized applications to access real-time vehicle status, remote control features, location data, electric vehicle charging status, climate control, and trip history for Toyota and Lexus connected vehicles.

- **Human URL:** [https://developer.eig.toyota.com/](https://developer.eig.toyota.com/)

#### Tags

- Automotive
- Connected Car
- Remote Control
- Vehicle Status
- EV

#### Properties

- [Documentation](https://developer.eig.toyota.com/)
- [OpenAPI](openapi/toyota-connected-services-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/toyota-connected-services.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/toyota-connected-services.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Toyota Dealers API

Toyota Dealers API enables searching and retrieving dealer information including location, hours, services offered, and inventory. Supports dealer locator applications and service scheduling integrations for Toyota and Lexus dealers.

- **Human URL:** [https://developer-sb.eig.toyota.com/apis/dealer](https://developer-sb.eig.toyota.com/apis/dealer)

#### Tags

- Automotive
- Dealers
- Dealer Locator
- Service
- Inventory

#### Properties

- [Documentation](https://developer-sb.eig.toyota.com/apis/dealer)
- [Postman Collection](collections/toyota-connected-services.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/toyota-connected-services.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/toyota-telematics.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/toyota-telematics.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/TOYOTA)
- [Website](https://developer.eig.toyota.com/)
- [Developer](https://developer.eig.toyota.com/)
- [Documentation](https://developer.eig.toyota.com/apis)
- [LinkedIn](https://www.linkedin.com/company/toyota-motor-corporation)
- [Rules](rules/toyota-spectral-rules.yml)
- [Vocabulary](vocabulary/toyota-vocabulary.yml)
- [J S O N L D Context](json-ld/toyota-context.jsonld)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
