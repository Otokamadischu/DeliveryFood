<h1 align="center">Delivery Food Application :pizza:</h1>

The food ordering and delivering application. It is self made application that allows restaurants add orders to the system that will be delivered by actually active couriers. Application thanks to the vehicle routing algorithm, finds the best routes, connects orders and assigns them to appropriate couriers.


<h1 align="center"><img src="https://user-images.githubusercontent.com/49680011/115531447-1456ed00-a295-11eb-84e2-9b0e3416aa2a.png" width="280" height="500"/></h1>



## Table of contents

- [Technologies](#technologies)
- [Description](#description)
- [Algorithm](#algorithm)
- [Images](#images)

## Technologies

- Java
- OSRM
- Jsprit
- Spring Boot
- Srping Data JPA
- Spring Security
- Java JWT
- Android
- SQL

## Description

The backend is written in Java, uses Spring Framework, and saves the data in MySQL. The view layer, on the other hand, is created for phones with the android system, it has a version for restaurant, courier and administrator. The program allows the restaurant to enter customer data and order details into the system, then a customer's address is converted into geographic coordinates. After receiving the order data, the server searches for all routes times between restaurants, clients and couriers from own Open Source Routing Machine server. The algorithm written using the Jsprit library, having all the necessary information, looks for the best combinations of routes for couriers, combines orders with each other to make couriers more efficient, and during small traffic it focuses primarily on fast delivery. The courier's application sends its location regularly to the server, and when the courier is assigned to the order, relevant information about the order appears. During the order courier still sends a location from which the estimated time of the courier's arrival can be calculated. All this is supervised thanks to the admin application who can cancel the order and change the order data at any time. The administrator can manage breaks for couriers, and then the algorithm knows that the courier will be unavailable for a specified period of time. The admin can view order histories at any time, as well as generate an excel file from a given order period, which is necessary during settlements with restaurants.

## Algorithm

Route assignment algorihtm takes into account:
- distance between restaurants, couriers and customers
- maximum delivery time
- time a meal is held by courier
- the maximum number of meals a courier can take
- ensures fast delivery when there is no heavy traffic
- connects and assigns orders in real time
- orders for the indicated time and without delivery time

## Images

<p float="center">
  <img src="https://user-images.githubusercontent.com/49680011/115953743-7b6ede80-a4ed-11eb-9fb9-34e1ccfd4e6c.png" width="280" height="500"/>
  <img src="https://user-images.githubusercontent.com/49680011/115953745-7c077500-a4ed-11eb-9d9e-a15985d2adca.png" width="280" height="500"/> 
  <img src="https://user-images.githubusercontent.com/49680011/115953746-7c077500-a4ed-11eb-8446-41b9953ba896.png" width="280" height="500"/>
</p>
