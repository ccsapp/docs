# Use Case "Remove Car from Fleet"

```
Title: Remove Car from Fleet

Primary Actors: Fleet Manager

Preconditions:
    - The given car is part of the fleet 
Postconditions:
    - The given car is no longer part of the fleet

Flow:
1. Actor deletes a car from the fleet by choosing a car from the fleet overview
2. System removes the car from the fleet
3. System presents user with option to undo deletion within five seconds
4. Actor waits for undo period to end without requesting undo

Alternative flows:
2a. System detects that the given car is not present in the fleet (probably removed by another parallel request)
    2a1. System informs user of the failure to remove the car and stops the use case
2b. System detects an error in the communication with the backend
    2b1. System informs user about the failed communication and stops the use case
4a. User requests undo
    4a1. System adds car to the fleet again
4a1a. System detects an error in the communication with the backend
    4a1a1. System informs user about the failed communication and stops the use case
```
