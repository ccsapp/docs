# Use Case "View Fleet Overview"

```
Title: View Fleet Overview

Primary Actors: Fleet Manager
Secondary Actors: Rental System 

Preconditions: 
    - System has a fleet registered for the actor 
Postconditions: 

Flow:
1. Actor requests an overview of the cars in the fleet from the system
2. System gathers rental data from the rental system
3. System gives a list of all cars with their VIN, brand, model, production date, and rental period to the actor

Alternative flows:
2a. System detects failure to communicate with the rental system 
    2a1. System signals error to the actor and stops the use case 
3a. There is a car in the list which is not rented at the time
    3a1. System leaves out the rental period and indicates that the car is unoccupied
3b. Actor selects a car from the list
    3b1. Actor starts the use case "View Car Status" 

Information Requirements: 
    Rental System:
    - Rental data: VIN, rental period
```