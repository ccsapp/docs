# Use Case "Create Car Rental"

```
Title: Create Car Rental

Primary Actors: Customer
Secondary Actors:

Preconditions:
Postconditions:
    - A new rental is created

Flow:
1. Actor requests cars available for rent in a given time period
2. System displays all cars with brand, model and number of seats available during the whole period
3. Actor selects a car from the list
4. System displays brand, model, color, weight, trunkVolume, engine type and power, transmission type, number of seats, number of doors, fuel type, fuel capacity, city, overland, and combined consumption and emissions of the selected car
5. Actor requests to rent the given car during the given period
6. System creates a new rental for the car for the time period and reports success

Alternative flows:
2a. Given the system detects failure to communicate with the connected car system
    2a1. System signals error to the actor and stops the use case
2b. Given no car is available in the period
    2b1. System informs the actor that no car is available and stops the use case
4a. Given the system detects failure to communicate with the connected car system
    4a1. System signals error to the actor
6a. System fails to create the rental
    6a1. System signals error to the actor and stops the use case

Information Requirements:
    Connected Car System:
    - Static car data: brand, model, color, weight, trunkVolume, engine type and power, transmission type, number of seats, number of doors, fuel type, fuel capacity, city, overland, and combined consumption and emissions
```
