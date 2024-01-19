# Route4Me API Summary

## Intro
[Route4Me](https://www.route4me.com/) helps businesses with route planning and optimization. By using Route4Me, businesses can efficiently scale and deliver reliable service to their customers. The platform streamlines essential last-mile workflows, including dispatch, tracking, driver performance, delivery management, and customer engagement. 

Key benefits of the Route4Me platform are:

- **Dynamic Route Optimization** - Build routes for multiple addresses and drivers, considering order time slots, vehicle restrictions, driver schedules, road conditions, no-go zones, and other factors.
- **All-in-one solution** - Integrate planning, dispatch, execution, and post-execution functionalities into a unified environment.
 - **Cloud-based** - A cloud-based system with native high availability, disaster recovery, and multiple geographically distributed servers. 

To use the Route4Me platform, you have two options. You can either access it through the web and mobile applications provided by Route4Me, or you can integrate it with your own software. If you choose to integrate it, Route4Me offers an Application Programming Interface (API) to make the process easier. This API is RESTful, meaning that you can use all of Route4Me's services via web requests and responses.

## Authentication
Before using the Route4Me API, you must first register for a [Route4Me account](https://route4me.com/login) and obtain an API Key. 
![Getting API key](https://support-cdn.route4me.com/2022/04/bb7d41db-route4me-api-key.jpg)
The API Key must be included as part of the query string in all API requests to the server.


## Platform API’s
All the abilities of Route4Me service are grouped into several Platform API endpoints described below. 

### Optimizations
Holds methods to manipulate route optimizations. In this context, optimization attempts to divide multiple addresses to be visited into several [routes](#routes) for delivery [vehicles](#vehicles). At that optimization should take into account order time slots, vehicle restrictions, driver timetables, road limitations, avoidance zones, and many other factors. You can create new optimization, remove existing optimization, retrieve optimizations, append and remove addresses from the optimization, and recalculate the optimal routes.

**Endpoint URL:** `https://route4me.com/api.v4/optimization_problem.php`

### Routes
Holds methods to manipulate routes. In this context, a route is a sequenced collection of one or more addresses that are assigned to a particular vehicle. You can create, update, duplicate, share, merge, or remove routes, append or remove addresses to a route, as well as change the order of addresses within the route.

**Endpoint URL:** `https://route4me.com/api.v4/route.php`

### Addresses
Describes some particular location. This could be destination, pick-up or drop-off point, warehouse, depot, customer address, and so on. Each address entity holds information about street name and number, city, state, country, and ZIP Code. Additionally, it may hold a number of other data: contact info, priority, geographic coordinates, reference number, and many more. To manage addresses you can use the [Address Book](#address-book) API.

**Endpoint URL:** `https://route4me.com/api.v4/address.php`

### Orders
Holds methods to manipulate orders. You can create ordinary or scheduled orders, add them to routes, update order information, and delete orders.

**Endpoint URL:** `https://route4me.com/api.v4/order.php`

### Tracking
Holds information about vehicle or asset tracking. For vehicles, this could include GPS location, speed, course, and possibly other [telematics data](#telematics-connections). For assets, this could include a tracking number or ID.

**Endpoint URL:** `https://route4me.com/api.v4/status.php`

### Telematics Connections
Holds methods to create, edit, and delete connections between Route4Me accounts and third-party telematics vendors. Typically, telematics systems collect real-time data from vehicle sensors, engine diagnostics, and GPS.

**Endpoint URL:** `https://oa.route4me.com/api/v1/user/telematics-connections`

### Members
Describes accounts and users of the Route4Me platform. In this context, accounts relate to some high-level entity (company, branch, department), and may have multiple users with different roles and access permissions (driver, dispatcher, manager, etc.) You can create, update, or remove accounts and users, as well as authenticate users.

**Endpoint URL:** `https://api.route4me.com/api.v4/user.php`

### Notes
Holds methods to create, edit, and delete any additional text or file data related to routes or addresses. 

**Endpoint URL:** `https://api.route4me.com/actions/addRouteNotes.php`

### Vehicles
Holds methods to manipulate vehicles. You can create, update, or remove particular vehicles, as well as assign them to routes.

**Endpoint URL:** `https://wh.route4me.com/modules/api/v5.0/vehicles`

### Commercial Routing
Describes different types of commercial vehicles.

**Endpoint URL:** `https://wh.route4me.com/modules/api/v5.0/vehicles`

### Activity Feed
Describes any routing activity related to a Route4Me account or team. This can include, route changes, drivers arriving at their destinations, entering or leaving geofence areas, adding notes, and so forth.

**Endpoint URL:** `https://api.route4me.com/api/get_activities.php`

### Address Book
A collection of location addresses. You can create new locations, update or delete existing locations, and search for locations that meet some specific criteria. Besides, you can group addresses into different categories using the [Address Book Group](#address-book-group) API.

**Endpoint URL:** `https://api.route4me.com/api.v4/address_book.php`

### Address Book Group
Describes a particular subcategory of addresses. You can create new groups, update or delete existing groups, retrieve group information, as well as retrieve address book contacts belonging to a specific group.

**Endpoint URL:** `https://api.route4me.com/api.v4/address_book_group.php`

### Avoidance Zones
A collection of zones or territories to avoid. This could be, for example, restricted areas, toll roads, high-traffic districts, no trucks allowed areas, and so forth. You can create, update, or remove avoidance zones, as well as obtain zone data. 

**Endpoint URL:** `https://api.route4me.com/api.v4/avoidance.php`

### Territories
Provides a way to divide your service area into smaller areas. Later on, you may assign a particular territory to particular drivers, branch offices, warehouses and so on. You can create, update, or remove territories, as well as retrieve territory data.

**Endpoint URL:** `https://api.route4me.com/api.v4/territory.php`

### Geocoding
Holds methods for converting addresses or place names into geographic coordinates and vice versa. 

**Endpoint URL:** `https://api.route4me.com/api/geocoder.php`


## SDKs
To make it easier to interact with Route4Me API from applications, we provide bindings for various programming languages and frameworks such as [C#](https://github.com/route4me/route4me-csharp-sdk), [C++](https://github.com/route4me/route4me-cpp-sdk), [C](https://github.com/route4me/route4me-c-sdk), [Java](https://github.com/route4me/route4me-java-sdk), [Node.js](https://github.com/route4me/route4me-nodejs-sdk), [PHP](https://github.com/route4me/route4me-php-sdk), [Python](https://github.com/route4me/route4me-python-sdk), [cURL](https://github.com/route4me/route4me-curl), [Ruby](https://github.com/route4me/route4me-ruby-sdk)
[Perl](https://github.com/route4me/route4me-perl-sdk), [Erlang](https://github.com/route4me/route4me-erlang-sdk), [F#](https://github.com/route4me/route4me-fsharp), [VB.NET](https://github.com/route4me/route4me-vbnet-sdk), [VBScript](https://github.com/route4me/route4me-vbscript-sdk), [Golang](https://github.com/route4me/route4me-go-sdk), and [Delphi](https://github.com/route4me/route4me-delphi-sdk). 

For example, the following code demonstrates how to build an optimal route using Route4Me Java SDK:
```java
import com.route4me.sdk.exception.APIException;
import com.route4me.sdk.services.routing.Constants.*;
import com.route4me.sdk.services.routing.*;
import java.util.ArrayList;
import java.util.List;

public class RouteOptimization {

    public static void main(String[] args) {
        // Specify API key
        String apiKey = "333333333333333333333DDD11111111";	
		// Create a Route4Me RoutingManager instance
        RoutingManager manager = new RoutingManager(apiKey);
		
		// Specify Optimization parameters
        OptimizationParameters optParameters = new OptimizationParameters();

        Parameters parameters = new Parameters();
        parameters.setAlgorithmType(AlgorithmType.CVRP_TW_SD.getValue());
        parameters.setStoreRoute(Boolean.FALSE);
        parameters.setShareRoute(Boolean.FALSE);
        parameters.setRouteName("Single Depot, Multiple Driver");
        parameters.setTravelMode(TravelMode.DRIVING.toString());

        // Specify delivery addresses
		List<Address> addresses = new ArrayList<>();
        addresses.add(new Address("1604 PARKRIDGE PKWY, Louisville, KY, 40214", true, 38.141598, -85.793846, 300));
        addresses.add(new Address("1407 MCCOY, Louisville, KY, 40215", 38.202496, -85.786514, 300));
        addresses.add(new Address("730 CECIL AVENUE, Louisville, KY, 40211", 38.248684, -85.821121, 300));
        addresses.add(new Address("4629 HILLSIDE DRIVE, Louisville, KY, 40216", 38.176067, -85.824638, 300));
        addresses.add(new Address("4738 BELLEVUE AVE, Louisville, KY, 40215", 38.179806, -85.775558, 300));

        optParameters.setAddresses(addresses);
        optParameters.setParameters(parameters);

        try {
			// Perform route optimization
            DataObject responseObject = manager.runOptimization(optParameters);
			
            System.out.println("Optimization Problem ID:" + responseObject.getOptimizationProblemId());
            System.out.println("State:" + OptimizationState.get(responseObject.getState().intValue()));
            if (responseObject.getAddresses() != null) {
                for (Address address : responseObject.getAddresses()) {
                    System.out.println(address);
                }
            }
        } catch (APIException e) {
            // Handle exception
            e.printStackTrace();
        }
    }
}
```
