# Toyota

Toyota Motor Corporation is a Japanese multinational automotive manufacturer that designs, manufactures, and sells vehicles including cars, trucks, and buses. Founded in 1937, Toyota is one of the largest automakers in the world, known for reliability, innovation, and commitment to sustainability. Toyota's developer platform provides APIs for vehicle lifecycle management, telematics, connected services, dealer data, and fleet management.

**Developer Portal:** [https://developer.eig.toyota.com/](https://developer.eig.toyota.com/)
**API Catalog:** [https://developer.eig.toyota.com/apis](https://developer.eig.toyota.com/apis)

---

## APIs

### Toyota Vehicle API

Vehicle lifecycle API providing information from initial order through retail sale for Toyota North America vehicles.

- **Documentation:** [https://developer.eig.toyota.com/apis/vehicle](https://developer.eig.toyota.com/apis/vehicle)

### Toyota Telematics API

Connected services subscriptions, satellite radio status, vehicle health data, GPS location, telemetry, and trip history for enrolled fleet vehicles.

- **Documentation:** [https://developer.eig.toyota.com/apis/telematics](https://developer.eig.toyota.com/apis/telematics)
- **OpenAPI Spec:** [openapi/toyota-telematics-openapi.yml](openapi/toyota-telematics-openapi.yml)

### Toyota Connected Services API

Real-time vehicle status, remote commands (lock/unlock, horn), climate pre-conditioning, EV battery/charging status, notifications, and service history for Toyota and Lexus connected vehicles.

- **Documentation:** [https://developer.eig.toyota.com/](https://developer.eig.toyota.com/)
- **OpenAPI Spec:** [openapi/toyota-connected-services-openapi.yml](openapi/toyota-connected-services-openapi.yml)

### Toyota Dealers API

Dealer search, location, hours, services, and inventory for Toyota and Lexus dealerships.

- **Documentation:** [https://developer-sb.eig.toyota.com/apis/dealer](https://developer-sb.eig.toyota.com/apis/dealer)

---

## Artifacts

### OpenAPI Specifications

| File | API | Description |
|---|---|---|
| [toyota-telematics-openapi.yml](openapi/toyota-telematics-openapi.yml) | Telematics | Fleet vehicle telematics and subscription data |
| [toyota-connected-services-openapi.yml](openapi/toyota-connected-services-openapi.yml) | Connected Services | Real-time vehicle status and remote control |

### Naftiko Capabilities

**Workflow Capabilities:**

| File | Description |
|---|---|
| [capabilities/fleet-management.yaml](capabilities/fleet-management.yaml) | Toyota fleet management and vehicle monitoring (12 tools) |
| [capabilities/connected-vehicle.yaml](capabilities/connected-vehicle.yaml) | Personal connected vehicle owner workflow (14 tools) |

**Shared Per-API Definitions:**

| File | API |
|---|---|
| [capabilities/shared/telematics.yaml](capabilities/shared/telematics.yaml) | Toyota Telematics |
| [capabilities/shared/connected-services.yaml](capabilities/shared/connected-services.yaml) | Toyota Connected Services |

### JSON Schemas

| File | Resource |
|---|---|
| [json-schema/toyota-vehicle-schema.json](json-schema/toyota-vehicle-schema.json) | Connected Vehicle |
| [json-schema/toyota-electric-status-schema.json](json-schema/toyota-electric-status-schema.json) | Electric Status (EV/Hybrid) |

### JSON Structure

| File | Resource |
|---|---|
| [json-structure/toyota-vehicle-structure.json](json-structure/toyota-vehicle-structure.json) | Connected Vehicle |

### JSON-LD Context

| File | Description |
|---|---|
| [json-ld/toyota-context.jsonld](json-ld/toyota-context.jsonld) | Linked data context mapping Toyota vehicle resources to schema.org |

### Examples

| File | Operation |
|---|---|
| [examples/toyota-get-electric-status-example.json](examples/toyota-get-electric-status-example.json) | Get Electric Status |
| [examples/toyota-send-remote-command-example.json](examples/toyota-send-remote-command-example.json) | Send Remote Command (Lock) |

### Spectral Rules

| File | Description |
|---|---|
| [rules/toyota-spectral-rules.yml](rules/toyota-spectral-rules.yml) | API design rules for Toyota OpenAPI specifications |

### Vocabulary

| File | Description |
|---|---|
| [vocabulary/toyota-vocabulary.yml](vocabulary/toyota-vocabulary.yml) | Domain vocabulary for Toyota connected vehicle and telematics APIs |

---

## Tags

`Automobiles` `Cars` `Vehicles` `Connected Car` `Telematics` `Fleet Management` `Electric Vehicles`
