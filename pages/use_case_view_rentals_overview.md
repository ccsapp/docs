# Use Case "View Rentals Overview"

```
Title: View Rentals Overview

Primary Actors: Customer
Secondary Actors: Connected Car System

Preconditions: 
Postconditions: 

Flow:
1. Actor requests an overview of their rentals from the system
2. System gives a list of all rentals with the rental period and car with its brand and model to the actor

Alternative flows:
2a. System detects failure to communicate with the connected car system 
    2a1. System signals error to the actor and stops the use case 

Information Requirements: 
    Connected Car System:
    - Static car data: brand, model
```

