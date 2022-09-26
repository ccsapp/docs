# Use Case Diagram (V1)

The use cases are further described below and are independent of a concrete case study. The use cases are grouped into the capability they belong. The capability "Management of Fleet" includes the functionality that a fleet manager needs to control (i.e., add and remove cars from the fleet) and to monitor (i.e., get the relevant information) the fleet. The capability "Management of Rental Services" grants customers additional services for the rental cars.

![](../figures/use_case_diagram.png)

## Use Cases

[(Add Car to Fleet)](use_case_add_car_to_fleet.md) A car is added to the fleet with its static car data such as vin, brand, model, fuel type is stored. Each car has its own fleet id. The static car data is not entered manually but is received from the system Connected Car. 

([Remove a Car from Fleet](use_case_remove_car_from_fleet.md)) A car which is removed from the fleet is no longer available in the fleet overview.

([View Fleet Overview](use_case_view_fleet_overview.md)) A fleet manager can list cars of the fleet based on search criteria which belong to the company. This fleet overview contains the static information of a car (such as VIN, brand, model, construction year, and existing rentals). 

## Involved External Systems
The following external systems are required to fulfill the requirements.

| Abstract External System | Concrete External System(s) | Description                                                                                                                                                       |
| ------------------------ | --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Connected Car System     | DaimlerCar                  | Each concrete connected car system has its own API for their cars.                                                                                                |
| Rental System            | CSOERentalDB                | The company CSOE has its own rental system which contains a database with the rental periods of each car and the corresponding customer (including past rentals). |