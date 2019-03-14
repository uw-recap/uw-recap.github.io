---
layout: post
title:  "In Car Testing: Session 2"
date:   2019-03-06 22:00:00 -0500
tags: RECAP testing
---
Based on the results of [Monday’s test](/2019/03/04/In-Car-Testing-1.html) we were able to implement a rudimentary risk calculation based on the distance between two vehicles and the speed of the following vehicle. This algorithm computes a safe following distance based on the vehicle’s current speed and a constant minimum safe time. If the car is following closer than this minimum distance than a risk value is presented to the user.

Additionally, we have been able to verify that heading data can be accurately obtained from the GPS and have figured out how to filter the velocity difference obtained from OBDII data to obtain a smooth value for acceleration. Now we can determine the relative range, bearing, velocity and acceleration between two vehicles. These are all of the parameters required to calculate a more accurate risk of collision using linear kinematic equations.

<div class="iframe-wrapper">
  <iframe src="https://drive.google.com/file/d/1o7S04sx3sZKUfB9xRli9ynuYExmlkW9G/preview" allowfullscreen></iframe>
</div>
