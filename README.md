# Generic Event Framework Use Case

## Objective

Create ability for application to allow other systems to react to events created within it without polling the master system.  

Consumers can be diverse from windows, web or workflow applications. They can be slow or fast. Framework should cater to all the consumers.

There is also possibility that some consumers may stop or disconnect but they should not miss any notifications.

The solution should be responsive, efficient, scalable and reliable.

## Application Information

The application under consideration is an existing Manufacturing Execution System (MES). It is a computerized system used in manufacturing to track and document the transformation of raw materials to finished goods. MES works in real time to enable the control of multiple elements of the production process (e.g. inputs, personnel, machines and support services)

MES application sits between the L2 layer like SCADA (Supervisory control and data acquisition) and L4 layer like ERP (Enterprise resource planning).

## Problem

MES is an enterprise application which keeps track of all the activity on the plant floor. This information is stored in 3M MES database and can be fetched by other systems only through the mechanism of REST based web services.

External systems need to poll the MES application for any changes that have happened in the system. This causes a large amount of API calls to the MES system just to get information for any changes in the system.

## Solution

Create ability in MES to inform external applications on any changes in MES as soon as they happen without the external applications polling MES.

MES records events related to process order status changes, batch events, stock events, inventory events, validated document changes, process variable changes, input consumption and output production events. 

## Architecture Review

1. Synchronous Communication

2. Asynchronous Communication

3. Push vs Pull

## Product Selection - Apache Kafka

## Architecture and Components

## Implementation

1. Apache Kafka

2. Docker





