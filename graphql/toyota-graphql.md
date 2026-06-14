# Toyota Motor GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Toyota Motor connected vehicle and telematics API surface, covering the Toyota Developer Portal (developer.eig.toyota.com). It unifies the Vehicle, Telematics, Connected Services, and Dealer APIs into a single graph that authorized applications can traverse.

Toyota's connected platform enables dealers, fleet managers, insurance telematics providers, and third-party developers to access real-time vehicle status, remote control features, EV charging data, trip history, maintenance alerts, and dealer information for Toyota and Lexus vehicles enrolled in connected services.

## Schema Source

Conceptual schema derived from:

- Toyota Vehicle API — https://developer.eig.toyota.com/apis/vehicle
- Toyota Telematics API — https://developer.eig.toyota.com/apis/telematics
- Toyota Connected Services API — https://developer.eig.toyota.com/
- Toyota Dealers API — https://developer-sb.eig.toyota.com/apis/dealer

## Authentication

Toyota's developer APIs use OAuth 2.0 client credentials flow for server-to-server access and authorization code flow for owner-consent connected services. API keys are issued per application through the Toyota Developer Portal.

## Root Types

### Query

- `vehicle(vin: String!)` — Retrieve a vehicle record by VIN
- `connectedVehicle(vin: String!)` — Real-time status and remote capabilities for an enrolled connected vehicle
- `vehicleStatus(vin: String!)` — Snapshot of current vehicle state (doors, locks, fuel, battery, HVAC)
- `vehicleLocation(vin: String!)` — Current GPS location and heading
- `tripHistory(vin: String!, limit: Int, offset: Int)` — Paginated list of recorded trips
- `fuelHistory(vin: String!, days: Int)` — Fuel consumption history
- `energyHistory(vin: String!, days: Int)` — EV/hybrid energy usage history
- `maintenanceAlerts(vin: String!)` — Active maintenance reminders and alerts
- `vehicleHealth(vin: String!)` — DTC codes, oil life, tire pressure, recall status
- `dealer(dealerCode: String!)` — Single dealer by Toyota dealer code
- `dealerLocator(zip: String!, radius: Int, brand: BrandEnum)` — Find dealers near a location
- `serviceHistory(vin: String!)` — Past service appointments recorded in the Toyota network
- `recalls(vin: String!)` — Open safety recalls for a vehicle
- `evRange(vin: String!)` — Estimated EV and hybrid range based on current battery and fuel
- `connectedServicesPackage(vin: String!)` — Enrolled connected services subscription status

### Mutation

- `remoteStart(vin: String!, input: RemoteStartInput!)` — Send a remote engine start command
- `lock(vin: String!)` — Lock all doors remotely
- `unlock(vin: String!, zone: UnlockZoneEnum)` — Unlock doors remotely
- `setClimateControl(vin: String!, input: ClimateControlInput!)` — Pre-condition cabin temperature
- `setChargeSettings(vin: String!, input: ChargeSettingsInput!)` — Update EV charge preferences
- `scheduleCharge(vin: String!, input: ChargingScheduleInput!)` — Set timed charge schedule
- `bookServiceAppointment(input: ServiceAppointmentInput!)` — Schedule a dealer service visit

### Subscription

- `vehicleStatusChanged(vin: String!)` — Real-time push when vehicle state changes
- `locationUpdated(vin: String!)` — Live location stream while vehicle is active
- `chargingStatusChanged(vin: String!)` — EV charge state changes (plug in/out, charge complete)
- `maintenanceAlertTriggered(vin: String!)` — New maintenance or health alerts

## Types Summary

| Type | Category |
|---|---|
| Vehicle | Vehicle Core |
| ConnectedVehicle | Vehicle Core |
| VIN | Vehicle Core |
| ToyotaVehicle | Vehicle Core |
| LexusVehicle | Vehicle Core |
| Model | Vehicle Core |
| Trim | Vehicle Core |
| Year | Vehicle Core |
| Engine | Vehicle Core |
| Battery | Vehicle Core |
| Drivetrain | Vehicle Core |
| Color | Vehicle Core |
| VehicleStatus | Status |
| IgnitionStatus | Status |
| DoorLockStatus | Status |
| WindowStatus | Status |
| TrunkStatus | Status |
| HoodStatus | Status |
| FuelLevel | Status |
| OdoReading | Status |
| BatteryLevel | EV / Hybrid |
| PlugStatus | EV / Hybrid |
| ChargeStatus | EV / Hybrid |
| ChargeSettings | EV / Hybrid |
| ChargingSchedule | EV / Hybrid |
| EVRange | EV / Hybrid |
| HybridRange | EV / Hybrid |
| HVAC | Climate |
| ClimateControl | Climate |
| RemoteStart | Remote Control |
| Remote | Remote Control |
| Lock | Remote Control |
| Unlock | Remote Control |
| ParkingBrake | Remote Control |
| EnhancedLocation | Location |
| GPSLocation | Location |
| NavigationRoute | Location |
| Trip | Telematics |
| TripRecord | Telematics |
| TripSummary | Telematics |
| DriveHistory | Telematics |
| FuelHistory | Telematics |
| EnergyHistory | Telematics |
| MaintenanceAlert | Maintenance |
| OilLife | Maintenance |
| TirePressure | Maintenance |
| Recall | Maintenance |
| DTCCode | Maintenance |
| VehicleHealth | Maintenance |
| ServiceReminder | Maintenance |
| DealerLocator | Dealer |
| Dealer | Dealer |
| ServiceHistory | Dealer |
| ServiceAppointment | Dealer |
| ConnectedServicesPackage | Subscription |
| Safety | Safety |
| SafetyConnect | Safety |
| Emergency | Safety |
| NightVision | Safety |
| BlindSpot | Safety |
| ToytaSafetyConnect | Safety |
| APIKey | Auth |
| Token | Auth |
| Webhook | Auth |

## Notes

- VIN-based access requires the vehicle to be enrolled in Toyota's connected services program.
- Remote commands (start, lock, unlock, climate) require owner-consent OAuth scope.
- Fleet and telematics endpoints use client-credentials scope with fleet enrollment.
- The Dealers API has a sandbox environment at developer-sb.eig.toyota.com.
- Lexus vehicles use the same underlying platform but may surface under a LexusVehicle type with brand-specific fields.
