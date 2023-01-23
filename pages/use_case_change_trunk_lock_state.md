# Use Case "Change Trunk Lock State"

```
Title: Change Trunk Lock State

Primary Actors: Trunk Opener
Secondary Actors: Connected Car System

Preconditions:
    - The actor has a permission to open the trunk of the car of a given rental for a given usage time
Postconditions:
    - The trunk lock state of the car associated with the associated rental changed

Flow:
1. Actor opens up the controls to the car trunk
2. System provides an overview page with the current trunk lock state
3. Actor requests to change the trunk lock state (via pressing a button)
4. System changes the trunk lock state and notifies the user the state changed succesfully

Alternative flows:
2a. Given the permission has expired
    2a1. System presents the user a notice that their permission expired and stops the use case
2b. System detects failure to communicate with the connected car system
    2b1. System signals error to the actor and stops the use case
4a. System detects failure to communicate with the connected car system
    4a1. System signals error to the actor and stops the use case
4b. Connected car system signals failure to change the trunk lock state
    4b1. System signals error to the actor and stops the use case

Information Requirements:
    Connected Car System:
    - Dynamic car data: trunk lock state
```
