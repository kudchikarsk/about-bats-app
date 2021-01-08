# About Product:

The product BATS is a menu driven enterprise Ad Scheduling and Billing software tailor made to the needs of broadcasters and radio operators. It has various modules associated with respective departments involved in Ad-Scheduling, Log Making and Billing.

It generates the final log as per the needs of the play-out systems which differs from client to client. The as-run log can be imported to generate the billing of the commercials played out. The system has an MIS system with comprehensive reporting and customised reporting.
The company has recently enhanced the product and made it available as SAAS for remote clients. The company is adding various value added elements to enhance the inventory sales, which will be announced recently.

# Challenges:

## Problem 1: Tightly coupled architecture
Current application is a traditional software made using two-tier architecture. In this architecture, the database acts as an integration database with application. This improves communication as the application is operating directly on persistent data. However there are downsides to this two tier architecture. 

When the application want to make changes to its data storage, it needs to coordinate with the application. This also means that the database usually cannot trust applications to update the data in a way that preserves database integrity and thus needs to take responsibility for that within the database itself.

Also, the structure that’s designed to integrate ends up being more complex—indeed, often dramatically more complex—than any single application needs.

## Problem 2: Classic windows applications
As the current product is classic window application its deployment is limited by Windows based system. Updates and installation must be manually implemented. If every client desktop gets a database connection, scaling is not good as database suffers from heavy load.

# Solution:

## Solution 1: Service-Oriented Architecture
The reengineering we did is shifted from integration database model to service-oriented
architecture

An interesting aspect of this shift to web services as an integration mechanism was that it resulted decoupling between internal database and the services with which
we talk to the application, the application doesn’t have to care how service store the data,
application directly talks with service.

Thus, database related modification can be made independenly to the the application. Allowing us to consider different strategies to store and retrieve data such as sharding, master-slave distribution (read scalability), and Peer-to-Peer Replication (write scalability). 

## Solution 2: Web application

Along with service oriented architecture we choose to go with web development environment for application.

First, the user doesn't have to download anything. This is one of the most appealing features of a web application. If designed correctly, websites can be built to be mobile compatible — compatible for just about any operating system or device. This eliminates the need to write a separate platform-specific applications. This also make deployment easy as updates are automatic and server side.


