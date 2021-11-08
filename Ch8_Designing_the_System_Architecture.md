# Chapter 8 : Designing the System Architecture

## 1. Introduction

Designing is about inventing the solution.
During design phase, we make certain technology choices (programming languages and DBMSs.)

---

## 2. Design Priorities

Within that architecture, we perform detailed design for the most
important use cases and partial design for the less important ones. Between increments, we
adjust the priorities, the urgencies and the design, as appropriate.

---

## 3. Steps in System Design

Steps are:
1. Choose a System Technology:
2. Making Technology Choices:
3. Designing a concurrency policy:
4. Designing a Security policy:
5. Choosing Subsystem Partition
6. Partitioning Subsystem into layers or other subsystems
7. Deciding how machines, subsystems and layers will communicate

---

## 4. Choosing a Networked System Topology

1. One-Tier Architecture:
  - Mainframe Model aka one-tier architecture.
  - Has no network in modern sense of networking
  - It is simple to setup


2. Two-Tier Architecture:
  - aka Client-Server architecture
  - Mini computers and workstations were introduced as client side
  - File Server, Midicomputer were introduced as server side
  - Introduced faster network
  - Introduced sophisticated graphics capabilities and window systems


3. Three-Tier Architecture:
  - Seperates **user-interface**, **program logic** and **data** in networked systems
  - Three tier -
    - Desktop Computers -> Client tier : presents user interface to the users.

    - Server -> Middle tier : aka. Business Logic tier, runs multithreaded program code and uses large processing power and memory.

    - Mainframe, Server -> Data tier : provides safe concurrent access to it.

    ### 1. Benefits of Three-Tier Architecture:

    1. Separation of concerns
    2. Using right machines for the job
    3. Improved performance : load balancing
    4. Improved Security
    5. Protection of investment
    6. Flexibility
    7. Accommodation of different types of client


4. Personal computers

5. Network computers

6. The Internet and WWW

7. Intranets

8. Extranets and VPNs:

    - Allows information to pass from firewall to firewall.

    - Uses Strong encryption to protect the information as it passes over the Internet.


9. Client-Server vs Distributed Architecture

  - Distributed also known as peer to peer architecture; grid computing

  - Eg. of Client Server architecture is E-commerce Model

  - Client-Server easier to build while Distributed is better at performance

10. Depicting Network Topology in UML

  System architectures can be depicted in UML on a **deployment diagram**.
  Simple deployment diagram shows only *nodes*, *communication path*, and *multiplicities*.


  ![UML deployment Diagram](resources/deploymentUML.png)




---

## 5. Designing for Concurrency

Most systems, especially networked systems, have many things happening at once; that is, they are concurrent systems.

**Note**: At a low level, database transactions and thread monitors are used to protect data inside individual processes, for example. At a higher level, we need to use *system rules* and *business rules* to control concurrent activity.

**Note**: we don’t inadvertently sell two tickets when there’s only one seat left. This is a process-level concurrency issue, because it can be controlled by the server process (the requests are serialized: the first to arrive gets the ticket, the second gets an error message).

-  The look and feel of a well-designed concurrent system is no different to the single-user
version.

- Our business services are the same for concurrent and single-user cases.

- To make a business object concurrent-safe, it’s only necessary to add messages and supporting objects; therefore, business messages (and associated attributes) can be designed
separately.

---

## 6.  Designing for Security
Five aspects of Security are:
1. **Privacy**

2. **Authentication**

3. **Irrefutability**

4. **Integrity**

5. **Safety** : We must be able to control access to resources (such as machines, processes, databases and files). Safety is also known as **authorization**.


First four requirements can be satisfied using digital encryption.

Operating System provides safety.

- ### General Security Rules
  -  Protect your servers from unauthorized access, whether accidental or malicious.

  - Confine sensitive information to your internal network: sensitive information includes details of business deals with other companies; business strategy; personnel details; details of the credit reference agencies you use; information relating to national security; and
  so on.

  - Prevent the eavesdropping of exported information: ensure that information you pass outside your intranet can only be read by the intended recipient.

  - Protect employee and customer passwords, which are not only the foundation of your entire security policy they’re often highly personal.

  -  Prevent server code accessing unneeded resources.

  -  Prevent client code accessing unneeded resources: we want to protect the client against unauthorized access to their resources and against accidental damage (because we want to offer a high quality of service and because we don’t want them to sue us if something goes wrong).

---

## 7. Partitioning Software


Breaking the business entities and business process into autonomous subsystems if necessary and into layers if necessary.


- ### Systems and Subsystems
A business should have a number of separate systems, each implemented by a different development team so that the temptation to reuse objects inappropriately is minimized. Then, where information needs to be passed between systems, it should pass in a well-defined, controlled manner via well-defined interfaces. In order to reduce complexity
further, each system should be broken down further into separate subsystems. Although each system has its own independent data, we can still use a single DBMS for deployment, since a DBMS will happily manage multiple databases.

- ### Layers
Each
layer is a cluster of collaborating objects dependent on the facilities offered by lower layers.
Layers don’t have to contain objects. For example, the Unix system library provides access
to low-level operating system facilities via a layer of C functions.

> A serious software system, even a small one by today’s standards, touches on so many areas that it would be impossible to guarantee its correctness by dealing with all components and properties on a single level. Instead, a layered approach is necessary, each layer relying on lower ones.

---


---

# Chapter 9 : Choosing Technologies

## 1. Introduction
---
## 2. Client Tier Technologies
---
## 3. Client Tier to Middle Tier Protocols
---
## 4. Middle Tier
---
## 5. Middle Tier to Data Tier Technologies
---
## 6. Other Technologies
---
## 7. Typical Front-End Configurations  
---
## 8. Back-End Configurations
---
## 9. Java E-Commerce Configurations
---
## 10. UML Packages
---
