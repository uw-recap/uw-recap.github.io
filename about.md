---
layout: page
title: About
permalink: /about/
---
## What is RECAP?
The Rear-End Collision Avoidance Project (RECAP) is a driver-aid that uses a network established between nearby vehicles to share and make use of other vehicles’ status information to improve drivers’ situational awareness. Determining how quickly a vehicle ahead is decelerating can be challenging, making it difficult for drivers to know how hard to brake. RECAP provides drivers with clear information, allowing them to make better, more informed driving decisions to avoid dangerous situations. With RECAP, drivers are more aware, making roads safer.

The choice of the name "RECAP" refers to this project being our Capstone Design Project, which is a chance for us to recap and apply all the knowledge we have gained throughout our years as Mechatronics Engineering students at the University of Waterloo.

## The Problem
Rear-end collisions between two vehicles are the most likely type of accident to occur: between 2007 and 2016, in Canada, **rear-end collisions between two vehicles represented 30% of all motor vehicle collisions** (according to data from the [National Collision Database Online](http://wwwapps2.tc.gc.ca/saf-sec-sur/7/ncdb-bndc/p.aspx?l=en)). We therefore decided to tackle rear-end collisions as a method of improving traffic safety.

## Existing Solutions
Some driver assistance systems have already been developed to tackle the problem of rear-end collisions:
- Adaptive Cruise Control (ACC): maintains a vehicle's cruising speed, but slows down if there is another vehicle ahead
- Forward Collision Warning (FCW): alerts a driver if they need to brake urgently to avoid a collision
- Automated Emergency Braking (AEB): automatically applies the brakes if the vehicle is about to collide with something
These systems have all been useful in reducing the number of rear-end collisions. But their major disadvantage is their **use of vision- or radar-based sensors** to determine the position of other vehicles and obstacles. These sensors can fail if the sensors don't have line of sight to obstacles, or if visibility is bad due to weather conditions.

## What does RECAP offer?
### Vehicle-to-Vehicle Communication
RECAP is based on **vehicle-to-vehicle (V2V) communication**: vehicles share data by transmitting it to other vehicles in the vicinity. Our prototype is able to handle information from vehicles within a 1 km radius. In our prototype design, RECAP will make vehicle speed and location data available to other vehicles, but this dataset can be expanded to include braking status, emergency vehicle alerts, and so on.

### Data Integration and Processing
The RECAP prototype includes a GPS unit and connection to the vehicle's OBD-II port, which gives it access to the vehicle's CAN bus. These sources give us information about the vehicle's position, speed, and acceleration. Using this data from one's own vehicle and surrounding vehicles, RECAP can determine which vehicles are in front of one's own vehicle, whether those vehicles are slowing down, and how fast they are slowing down. By combining this data, RECAP can notify a driver about the risk of collision with a vehicle ahead.

### Driver Notification and Alerting
RECAP presents the risk of collision with a vehicle ahead to the driver on a small LCD screen. The change of risk over time is also shown, so that the driver knows whether the situation has changed suddenly or gradually. We decided to have the prototype show the information to a human driver, rather than trying to automatically brake the vehicle, because until it is thoroughly tested, we assume that a human can make a more informed decision about whether to brake than RECAP can. We also want RECAP to promote safe driving behaviours by helping drivers better anticipate collisions with other vehicles.
