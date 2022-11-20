# Use Case "Remove Car from Fleet"

```
Title: Remove Car from Fleet

Primary Actors: Fleet Manager

Preconditions: 
    - The car with the given VIN is part of the fleet 
Postconditions: 
    - The car with the given VIN is no longer part of the fleet

Flow:
1. Actor deletes a car from the fleet by choosing a car from the fleet overview
2. System validates that the given VIN is valid and a car with the given VIN is present in the fleet
3. System prompts the user for confirmation
4. Actor confirms removal
5. System removes the car from the fleet

Alternative flows:
2a. Given VIN is invalid or a car with the given VIN is not present in the fleet (Probably an error of the front end)
    2a1. System informs user of the failure to remove the car and suggests trying again
2b. System detects an error in the communication with the backend.
    2b1. The system informs user about the failed communication and stops the use case
4a. Actor denies removal
    4a1. System stops the use case without removing the car

```
