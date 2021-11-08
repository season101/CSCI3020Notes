# Chapter 7 Analyzing the Problem

#### Analysis is the discovery of what system is going to handle.
- Decompose requirements into the essential elements and relationships.
- Modeling real world as objects.


#### An Analysis model has both static and dynamic parts.
- Static Analysis is done using Static Analysis Model using class diagram. Our Sponsors
will be able to confirm that our understanding of the business model is correct.

- Dynamic Analysis is done using Dynamic Analysis Model using Communication diagram. We
will be confident that our Analysis objects support the required system functionality.

---
## Two inputs to the Analysis:
  ##### 1. Business requirements Model
  ##### 2. System requirements Model

---

### Why do Analysis?
To design a solution before we understand the problem.

---

## Overview of the Analysis Process
1. Use the system requirements model to **find candidate classes** that describe the objects
that might be relevant to the system and **record them on a class diagram**.

2. **Find relationships (association, aggregation, composition and inheritance)** between the
classes.

3. **Find attributes** (simple, named properties of the objects) for the classes.

4. Walk through the system use cases, checking that they’re supported by the objects that
we have, **fine-tuning the classes, attributes and relationships** as we go – this use case
realization will produce operations to complement the attributes.

5. **Update the glossary and the non functional requirements as necessary** – the use cases
themselves should not need updating, although perhaps they will need some correcting.

---

## Static Analysis
It involves deciding the logical or physical parts and how they should be connected to each other.

#### 1. Finding Classes

- We have good source of possible candidates in the form of system use cases.

- Candidate Classes are often indicated by **nouns** in the use cases.

#### 2. Identifying Class relationships

There are four possible types of relationships:

1. Inheritance: A subclass inherits all of the attributes and behaviour of its superclass(es).

2. Association: Objects of one class are associated with the objects of another class.

3. Aggregation: Strong Association- an instance of one class is made up of instances of another class.

4. Composition : Strong Association- the composed objects can't be shared by other objects and die with its composer.

![Alternate Text: github.png](resources\Class Relationships.drawio.png)
