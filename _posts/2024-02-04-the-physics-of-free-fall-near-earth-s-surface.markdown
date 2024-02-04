---
layout: post
title: "The Physics of Free Fall Near Earth's Surface"
date: 2024-02-04 17:27:51 +0000
categories: "News"
excerpt_image: https://www.grc.nasa.gov/www/k-12/VirtualAero/BottleRocket/airplane/Images/mofall.gif
image: https://www.grc.nasa.gov/www/k-12/VirtualAero/BottleRocket/airplane/Images/mofall.gif
---

[Free fall acceleration equations derivation](https://fistore.mysenprints.com/collection/aldrete)
### Applying Newton's Second Law of Motion
According to Newton's second law of motion, force is equal to the mass of an object multiplied by its acceleration. For the force of gravity near Earth's surface, the gravitational force F is equal to the mass m multiplied by the gravitational acceleration g. This can be expressed as the equation F = m * g. 
We know that acceleration is the second time derivative of position. So setting this equal to the gravitational acceleration g, we get: m * dv/dt = m*g, where dv/dt is the rate of change of velocity with respect to time. Dividing both sides by the mass m, we are left with dv/dt = g. 

![](https://www1.grc.nasa.gov/wp-content/uploads/mofall.jpg)
### Integrating to Find Velocity
Integrating both sides with respect to time gives: ∫dv = ∫g dt. The integral of the left side is the change in velocity v. The integral of the right side is simply gravitational acceleration g multiplied by time t. This gives the equation: v = g*t + C, where C is the constant of integration. 
Since we are considering free fall starting from rest, the initial velocity v0 is zero. Therefore, we can set C = 0, giving the equation for velocity in terms of gravitational acceleration and time: v = g*t
### Another Integration to Find Position 
To find the equation for position, we integrate the velocity equation once more with respect to time. This gives: ∫v dt = ∫g t dt. The integral of velocity v is displacement x. The integral of g*t is (1/2)g*t^2. Once again, the constant of integration represents the initial position, which we set to zero since we are considering an object starting from rest at the surface. Therefore, the final equation for displacement due to gravity is: x = (1/2)g*t^2
**Applying the equations to calculate free fall distance** 
### Plugging in Known Values
Now that we have derived the key equation x = (1/2)g*t^2 to calculate displacement due to gravity, let's plug in values to solve a specific example. Near Earth's surface, gravitational acceleration g is approximately 9.8 m/s^2. Let's calculate the distance fallen after 3 seconds. 
Plugging the values into the equation, we get: x = (1/2) * 9.8 m/s^2 * (3s)^2 = 44.145 m
### Checking the Result Numerically 
We can check this result by calculating the distance fallen numerically as well. In the first second, the object falls 4.9 m due to accelerating from 0 to 9.8 m/s. In the second second it falls another 9.8 m, and it falls 19.6 m in the third second. Adding these components gives a total distance of 44.1 m, which matches our calculated result from the equation very closely.
**Applications of free fall equations**
### Modeling Projectile Motion 
The equations derived here for displacement under constant acceleration directly apply to modeling the vertical motion of projectiles under gravity near Earth's surface. By separating the vertical and horizontal components of motion, projectile problems can be modeled using these same equations.
### Calculating Terminal Velocity
These equations also provide the foundation for determining terminal velocity, the maximum speed attainable by an object in free fall due to air resistance balancing the force of gravity. Terminal velocity arises when the derivative of velocity with respect to time, the acceleration, reaches zero.
### Estimating Fall/Jump Distances and Times  
Simple rearrangements of the kinematic equations allow estimation of fall/jump distances from given heights or times, or computation of times from given distances. This has applications in safety planning for construction work, adventure activities like base jumping, and engineering ballistics problems.
### In Summary
In summary, through mathematically rigorous integration of Newton's second law of motion and gravitational acceleration, we have derived the fundamental equations governing one-dimensional free fall near Earth's surface. These equations provide powerful tools for modeling a wide range of physical phenomena involving falling or thrown objects.
![The Physics of Free Fall Near Earth's Surface](https://www.grc.nasa.gov/www/k-12/VirtualAero/BottleRocket/airplane/Images/mofall.gif)