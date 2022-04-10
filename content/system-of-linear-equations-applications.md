---
title: System of linear equations applications
aliases:
---
Status:
Tags: #cards/math232/unit2
Links: [System of linear equations](out/system-of-linear-equations.md)
___

# System of linear equations applications
> Learn the abstract so you can apply it to specific situations !

## Flow Networks
A flow network is a collection of branches through which something “flows”. The branches meet at nodes
- *ex) Electricity flowing through wires*
[![Image from Gyazo](https://i.gyazo.com/e806e0021126572b689457fb35d2a1ae.png)](https://gyazo.com/e806e0021126572b689457fb35d2a1ae)

### Properties
- **One-directional flow:** At any moment, the flow in each branch is in one direction only.
- **Flow conservation at nodes:** The rate of low into each node is equal to the rate of flow out of the node.
- **Flow conservation in the network:** The rate of flow in the network is equal to the rate of flow out of the network.

### Application
- Some flow of branches will be known, while others must be solved

Steps
?
1. Assume direction, if it is negative then just flip it
1. Assign variable names to unknown flows
1. Use conservation of flow at each node to generate as many equations as there are unknowns
	- *ex) 4 nodes = 4 equations*
1. Solve equation, get solution
<!--SR:!2022-02-20,10,150-->

### Examples
Find unknown flows
[![Image from Gyazo](https://i.gyazo.com/62827e52e9b2ed8c47610d5a0776dbd4.png)](https://gyazo.com/62827e52e9b2ed8c47610d5a0776dbd4)
?
- ref, back substitution
[![Image from Gyazo](https://i.gyazo.com/60b5c68ecfc2df5f344f6dfddeed555d.png)](https://gyazo.com/60b5c68ecfc2df5f344f6dfddeed555d)
[![Image from Gyazo](https://i.gyazo.com/3d74c1e08fdc9a2e1f956173f818f7c2.png)](https://gyazo.com/3d74c1e08fdc9a2e1f956173f818f7c2)
<!--SR:!2022-02-21,11,150-->

___

## Balancing Chemical Equations
[![Image from Gyazo](https://i.gyazo.com/8ec87dc160c30a30f90034f2cf34c835.png)](https://gyazo.com/8ec87dc160c30a30f90034f2cf34c835)
?
- Assign x variables alongside compound
	- Positive and integers
- 4 unknowns, 4 equations
	- Write equations for all elements, then move to LHS
[![Image from Gyazo](https://i.gyazo.com/7d1bf3ee0e861407e096186fa8894186.png)](https://gyazo.com/7d1bf3ee0e861407e096186fa8894186)
- Row reduce, back sub to find solution vector, each component is for each compound element in eqn
<!--SR:!2022-02-22,12,170-->

## Polynomial Interpolation
- Find a polynomial that goes through all points
- Intercept monomial is just 1
- Find degree (number of points)
- Setup equation to find each point where x and y are plugged into the equation
- [![Image from Gyazo](https://i.gyazo.com/d18cceb4c3c273bb124501b6c5fb3a57.png)](https://gyazo.com/d18cceb4c3c273bb124501b6c5fb3a57)
- 
[![Image from Gyazo](https://i.gyazo.com/eddc4b4bc4cbd8f5f999d51703a0e9f9.png)](https://gyazo.com/eddc4b4bc4cbd8f5f999d51703a0e9f9)
# Backlinks
```dataview
list from [System of linear equations applications](out/system-of-linear-equations-applications.md) AND !outgoing([System of linear equations applications](out/system-of-linear-equations-applications.md))
```
___
References:

Created:: 2022-01-22 23:11
