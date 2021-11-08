# Generic Event Framework

## __Objective__

Create ability for application to allow other systems to react to events created within it without polling the master system.  

Consumers can be diverse from windows, web or workflow applications. They can be slow or fast. Framework should cater to all the consumers.

There is also possibility that some consumers may stop or disconnect but they should not miss any notifications.

The solution should be responsive, efficient, scalable and reliable.

## __Application Information__

The application under consideration is an existing Manufacturing Execution System (MES). It is a computerized system used in manufacturing to track and document the transformation of raw materials to finished goods. MES works in real time to enable the control of multiple elements of the production process (e.g. inputs, personnel, machines and support services)

MES application sits between the L2 layer like SCADA (Supervisory control and data acquisition) and L4 layer like ERP (Enterprise resource planning).

## __Problem__

MES is an enterprise application which keeps track of all the activity on the plant floor. This information is stored in 3M MES database and can be fetched by other systems only through the mechanism of REST based web services.

External systems need to poll the MES application for any changes that have happened in the system. This causes a large amount of API calls to the MES system just to get information for any changes in the system.

## __Solution__

Create ability in MES to inform external applications on any changes in MES as soon as they happen without the external applications polling MES.

MES records events related to process order status changes, batch events, stock events, inventory events, validated document changes, process variable changes, input consumption and output production events. 

## __Architecture Review__
---


### 1. Synchronous Communication
---

In synchronous communication both the parties in the communication actively have an established channel and communicate over it with each other. 

In this case both the parties need to be continously listening over the channel and cannot disconnect and resume on a later point in time. 

This is more like a human to human interaction where both human need to be present for a conversation. One human requests for some information or provides some information and the other person responds with the information or acknowledges that he / she received the information.

Typically in software systems, these conversations are modelled using request / response based services like WCF (Windows Communication Foundation), RPC, Web APIs etc

![](src/images/SynchronousCommunication.png)

#### PROS

* Simple request / response based services
* Easy to develop, standardized .NET tools for creating services, widely used
* Easy to visualize, debug and direct communication
* Ideal for non-durable communication

#### CONS

* Tightly Coupled
* Wait time for consumer to accept, process and respond to request
* Blocking
* Latency (Dependency)
* Non-Durable - Consumer needs to be actively listening for requests

### 2. Asynchronous Communication
---


![](src/images/AsynchronousCommunication.png)

![](src/images/AsynchronousCommunication_Issue.png)

#### PROS

*
*
*

#### CONS

*
*
*

### 3. Push vs Pull
---

![](src/images/Push.png)

#### PROS

*
*
*

#### CONS

*
*
*

![](src/images/Pull.png)

#### PROS

*
*
*

#### CONS


*
*
*

## __Product Selection - Apache Kafka__

## __Architecture and Components__

## __Implementation__

1. Apache Kafka

2. Docker
