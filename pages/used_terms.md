# Used Terms

## Car-related Terms

The ubiquitous language defined in this documentation is the language foundation of the terms that are consistently used in the doamin ConnectedCar and in the applications residing to this domain. New applications can add additional terms to this foundation if the terms are application-agnostic and, threfore, needed by other applications that are based on the domain ConnectedCar.

| Term                | Definition                                                                                                                                     | Remarks                                                                                                                                         |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Brand               | Data that specifies the brand name of the Vehicle manufacturer                                                      |  
| Car                 | A specific type of vehicle                                                                                      | 
| Consumption         | Data that specifies the consumed fuel of the engine, expressed in units such as liters or kWh per kilometer     |
| Emissions           | Data that specifies the CO2 emitted by a Vehicle during operation in gram per kilometer                             | 
| Fleet               | A set of vehicles                                                                                               |
| Fuel                | Data that defines the source of energy that powers the Vehicle such as petrol or electric energy                                               | 
| Production Date             | Data that specifies the date on which the vehicle was fully assembled                                                             |  
| Technical Specification | Data of a Vehicle encapsulating the core physical makeup and performance of the vehicle                         | 
| Trunk               | A covered space of a Vehicle which is the main storage or cargo compartment | 
| Vehicle             | A physical unit which is used to transport persons and/or goods. Examples of vehicles are: bicycle, bus, car, train, truck            |    
| VIN | Data which uniquely identifies a Vehicle


## Application-related Terms

| Term               | Definition                                                                                       | Remarks |
| ------------------ | ------------------------------------------------------------------------------------------------ | ------- |
| Fleet Manager      | A role that owns one or more cars and rents them to customers                                    |         |
| Static Car Data    | Data containing static information on a car such as the VIN, brand, model, and construction year |         |
| Rental Period      | Data containing the start and end date of a car rental                                           |         |
| Active Rental      | A rental is active if the current date is between start and end date of the rental period        |         |
| Trunk Access       | A permission to open the trunk of a car which is explicitly granted to an external person        |         |
| Trunk Access Token | A 24-char alphanumeric proof of the trunk access                                                 |         |
| Trunk Permission   | A trunk access (explicitly granted) or the implicit permission of customer with active rental    |         |
