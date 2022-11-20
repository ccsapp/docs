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
2. System gives a list of all cars with their VIN, brand, model, and production date to the actor

Alternative flows:
2a. System detects failure to communicate with the rental system 
    2a1. System signals error to the actor and stops the use case 

Information Requirements: 
    Connected Car System:
    -  Static car data: VIN, brand, model, production date
```
