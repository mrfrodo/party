# Party

## Hexagonal architecture ports and adapter domain driven design
* application
* domain
* infrastructure
---
### Design
* Party entity: aggregate root: java record Party
* Telephone entity: aggregate: java record Telephone
* TelephoneNumber value object: java record TelephoneNumber
---
* Use case services (application)
* Domain services (domain)
* Rest contrllers and spring data jdbc (infrastructure)
  * Spring rest controller as primary driver in adapters  
  * Spring data jdbc as secondary driven out adapter
---

Party entity
* Long Id, PartyId partyId, Telephone
* Immutable, domain services, behavior, validation
---
PartyId value object
* String partyId
---
Telephone entity
* Long Id, TelephoneNumber telephoneNumber, String type
* Immutable, domain services, behavior, validation
---
TelephoneNumber value object
* String number