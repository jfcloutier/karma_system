# System

## About

* karma system
  * karma_agency (prolog)
    * App
    * Implements agency functions
      * Apperception
      * Fitness
      * Society of Mind (SOM)
        * Cognition actors
        * Metacognition
  * karma_body (elixir/phoenix)
    * Web app
    * Defines and operates physical or simulated sensors and actuators
      * List actuators and sensors as abstract devices
      * Sense and actuate on request
  * karma_world (elixir/liveview)
    * Web app
    * Provides an environment for simulated sensors and actuators
    * Visualiztion
  * karma_observer (elixir/liveview)
    * Web app
    * Monitoring of an karma_agency

## Status

* karma_agency - **under construction**
  * Operational
    * actor model framework
    * apperception engine
  * To do
    * SOM
    * Fitness and feelings
* karma_body - **under construction**
  * Operational
    * Lego sensors and actuators on a BrickPi3
  * To do
    * Simulated sensors and actuators
* karma_world - **under construction**
* karma_observer - **TO DO**

## Karma system

```mermaid
---
title: Networking
---

graph LR;
agency("`**agency**
*prolog on PC*`")==>|HTTP|body_on_brickpi3("`**body (physical)**
*elixir on brickpi3*`") & body_on_PC & observer("`**observer**
*elixir on PC*`") 
body_on_PC("`**body (simulated)**
*elixir on PC*`")==>|HTTP|world("`**world**
*elixir on PC*`")

```

----

``` mermaid
---
title: System components
---

classDiagram
  Agency
  Observer
  Body
  World
  Observer <-- Agency
  Body <--> World
  Body <--> Agency
  class Agency {
    on PC
    Prolog app
    apperception()
    fitness()
    som()
    pubsub()
    body_interface()
  }
  class Observer {
    on PC
    Elixir web ppp
    monitor()
  }
  class Body {
    sensors()
    actuators()
    sense(sensor)
    actuate(actuator, action)
  }
  class World {
    sensing(sensor)
    actuating(actuator, action)
    visualize()
  }

```

----

```mermaid
---
title: System interactions in the physical world
---

sequenceDiagram;
    participant agency
    participant body
    participant observer
    agency-->>+body: ask for actuators/sensors
    body-->>-agency: answer actuator/sensors
    agency-->>+body: sense/actuate
    body-->>-agency: sensed/actuated
    agency-->>observer: SOM or fitness event
    agency-->>agency: SOM or fitness event
```

----

```mermaid
---
title: System interactions in a simulated world
---

sequenceDiagram;
    participant agency
    participant body
    participant world
    participant observer
    agency-->>+body: ask for actuators/sensors
    body-->>-agency: answer actuator/sensors
    agency-->>+body: sense/actuate
    body-->>+world: sensing/actuating
    world-->-body: sensed/actuated
    body-->>-agency: sensed/actuated
    agency-->>observer: SOM or fitness event
    agency-->>agency: SOM or fitness event
```
