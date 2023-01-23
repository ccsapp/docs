# Use Case "Grant Trunk Access"

```
Title: Grant Trunk Access

Primary Actors: Customer
Secondary Actors: Connected Car System

Preconditions:
    - The actor has an active rental
Postconditions:
    - A permission to change the trunk lock state of a car is created

Flow:
1. Actor requests to give permission to access the trunk of a car valid for a given period of time
2. System creates a permission associated with the currently active rental and valid for the given period of time
3. System provides the user with an access to the newly created permission

Alternative flows:
2a. Given the actor does not have an active rental for the given car
    2a1. System asks the actor to provide another car and restarts the use case
2b. Given the rental already has a token associated with it
    2b1. System removes the old token before creating the new one
2c. Given the given period of time is longer than the remaining time of the rental
    2c1. System creates a permission associated with the rental and valid for the remaining time of the rental

Information Requirements:
    (none)
```

