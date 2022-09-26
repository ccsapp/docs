# Use Case "Add Car to Fleet"

```
Title: Add Car to Fleet

Primary Actors: Fleet Manager
Secondary Actors: Connected Car System

Preconditions: 
    - System has a fleet registered for the actor 
Postconditions: 
    - The car with the given VIN is added to the fleet
    - Static car data on the car with the given VIN is saved

Flow:
1. Actor adds a new car to the fleet by providing the VIN
2. System validates that the given VIN is valid and a car with the given VIN is not present in the fleet
3. System gathers static car data on the car with the given VIN from the connected car system 
4. System adds the car to the fleet with its VIN, brand, model and production date 

Alternative flows:
2a. Given VIN is invalid
    2a1. System prompts actor to re-enter the VIN
2b. A car with the given VIN is already present in the fleet
    2b1. System informs the actor that the car is already in the fleet and stops the use case
3a. System detects failure to communicate with the connected car system
    3a1. System signals error to the actor and stops the use case 
3b. Connected car system does not have a car with the given VIN
    3b1. System informs the actor that a car with the given VIN does not exist and stops the use case 


Information Requirements: 
    Connected Car System:
    -  Static car data: VIN, brand, model, production date
```