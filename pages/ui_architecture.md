# UI Architecture

The following architecture depicts V1.0 of the UI-CCSAppWeb. The architecture consists of the UI-CCSAppWeb itself and the relevant parts of the backend implemented using the Integration Platform as a Service (IPaaS) system MuleSoft.  To keep it simple, some elements were left out of the diagram. A more detailed version of this architecture can be found within the repository of the [UI](https://git.scc.kit.edu/cm-tm/cm-team/connectedcar/mulesoftarchitecture/CCSAppV1/presentation/uiccsappweb/-/blob/main/pages/architecture.md).

![](../figures/ui_architecture.png)

## UI-CCSAppWeb

The UI is implemented in Angular and consists of a variety of components that are responsible for displaying data; and services, which implement the necessary logic for fetching and updating the data.

### Component Login

The component Login displays a simple login page. Originally, the login page was connected to the identity provider Okta. In v1.0, the login is mocked and a button can be clicked to impersonate logging in as a certain user. Upon successful login, a JSON Web Token (JWT) is stored in the application's authentication context.

### Module AppRouting

The module AppRouting is responsible for mapping Angular components to routes. For example, the module maps the component Login to the route `/login`. It uses the underlying Angular Routing [Ang-Rou] module to achieve this, which provides further useful features. The router decides whether or not a user should be able to access a page based on their roles. The user's roles/groups are retrieved from the stored JWT in the application's authentication context.

### Component FleetOverview

The component FleetOverview is responsible for displaying fleet data. The view is only available to users with the role fleet manager. It displays a table that summarizes all of the vehicles in the manager's fleet and allows for adding and removing vehicles to the fleet. 


### Service Fleets

The service Fleets implements the backend communication required by the component FleetOverview. This includes the logic to fetch the fleet data from the backend and to send HTTP requests to add or remove cars from the fleet. Under the hood, the service uses Angular's HTTP client to perform the HTTP requests. The URL of the Experience API is injected into the service as an environment variable. 

The user's JWT needs to be sent with each request from the UI to the backend. Angular offers an elegant solution for this using so-called HTTP Interceptors, which doesn't require manual addition of the token to each request. An interceptor is implemented in the UI, which intercepts each outgoing HTTP request and injects the user's JWT into the authorization header of the request. The JWT is retrieved from the application's authentication context. 

## Backend Connection

The CCSApp backend is implemented using MuleSoft. For more information on the backend, refer to the relevant documentation [here](../README.md).
The relevant part for the UI is the Experience API E-CCSAppWeb. This API exposes the necessary endpoints for the UI and forwards any requests to the relevant backend Process APIs.

To get around Cross-Origin Resource Sharing (CORS) restrictions, a MuleSoft proxy A-CCSAppWeb is deployed ahead of the Experience API. The proxy receives requests from the UI, applies the configured policies, and forwards the requests to the Experience API.

## Abbreviations

- CCSAppOC ConnectedCarServicesApplicationOpenIDConnectClient
- CCSAppWeb ConnectedCarServicesApplicationWebInterface
- IPaaS Integration Platform as a Service
- JWT JSON Web Token
- MVP Minimum Viable Product
- OIDC OpenIDConnectClient
- UI User Interface

## Sources
- [Ang-Rou] Angular: RouterModule https://angular.io/api/router/RouterModule, accessed on: 2022-09-22.
