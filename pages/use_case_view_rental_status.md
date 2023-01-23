# Use Case "View Rental Status"

```
Title: View Rental Status

Primary Actors: Customer
Secondary Actors: Connected Car System

Preconditions: 
Postconditions: 

Flow:
1. Actor requests a status overview of a car by choosing a rental from the rentals overview
2. System presents a status view of the car containing the brand, model, color, weight, trunkVolume, engine type and power, transmission type, number of seats, number of doors, fuel type, fuel capacity, city, overland, and combined consumption and emissions. Fuel level percentage, position, trunk lock state, door lock state, and engine state are provided additionally if the actor currently rents the car. Lastly, the actor’s next rental period for this car is provided.

Alternative flows:
2a. Connected car system does not have a car with the given VIN
    2a1. System informs the actor that a car with the given VIN does not exist and stops the use case 
2b. System detects an error in the communication with the backend.
    2b1. System informs user about the failed communication and stops the use case

Information Requirements: 
    Connected Car System:
    - Static car data: VIN, brand, model, color, weight, trunk volume, engine type and power, transmission type, number of seats, number of doors, fuel type and capacity, consumption, emissions
    - Dynamic car data: fuel level percentage, position, trunk lock state, doors lock state, engine state
```
