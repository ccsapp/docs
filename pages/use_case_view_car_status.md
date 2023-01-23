# Use Case "View Car Status"

```
Title: View Car Status

Primary Actors: Fleet Manager
Secondary Actors: Connected Car System

Preconditions: 
    - System has a fleet registered for the actor

Flow:
1. Actor requests a status overview of a car by choosing a car from the fleet overview
2. System presents a status view of the car containing the brand, model, color, weight, trunkVolume, engine type and power, transmission type, number of seats, number of doors, fuel type, fuel capacity, fuel level percentage, position, trunk lock state, door lock state, tire type and manufacturer, VIN and production date, as well as city, overland and combined consumption and emissions. Lastly, the next active rental is provided with user and rental period.

Alternative flows:
2a. Connected car system does not have the given car
    2a1. System informs the actor that the given car does not exist and stops the use case 

Information Requirements: 
    Connected Car System:
    - Static car data: VIN, brand, model, production date, color, weight, trunk volume, engine type and power, transmission type, tire manfucaturer and type, number of seats, number of doors, fuel type and capacity, consumption, emissions
    - Dynamic car data: fuel level percentage, position, trunk lock state, doors lock state, engine state
```

