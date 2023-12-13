---
title: "Sensor Array Optimization for Industrial Robot"
excerpt: "<br/><img src='/images/Sensor_Array_1.png' width='500' height='500'>"
collection: projects
---
<figure style="width: 500px;">
    <img src='/images/Sensor_Array_2.png'>
    <figcaption>A render of a single sensor array disk. All credit for design, manufacturing, and production of the original disks should go to Colette Abah, Andrew Orekhov, and Garrison Johnston of ARMA labs.</figcaption>
</figure>

The ARMA lab at Vanderbilt has built a [manufacturing robot](http://arma.vuse.vanderbilt.edu/index.php/research?id=197) for confined spaces that allows for human-robot collaboration. The robot utilizes an array of Hall effect (touch) and Time-of-Flight (distance) sensors that facilitates safe interaction with humans and the environment. As an REU, I **refactored the code for modular sensing**, allowing specific sensors to be polled at varying intervals. This **improved latency by 60%** and facilitated more accurate movement and mapping of the surroundings. 

After refactoring and designing C++ and Arduino code to allow modular sensing, I conducted extensive sensor tests to determine response time bottlenecks. I built a testing rig with preset distances for the sensors to read from and gathered data for every possible combination of the eight sensors in a disk. Through this, I found that particular combinations of sensors could read almost as much data at a much faster rate, leading to gains in efficiency and speed when critical sensors were prioritized. Further, I programmed the use of both continuous and discrete polling modes from sensors, which would allow for pulling data from sensors without having to wait for every sensor to obtain their measurements.

This project had specific goals, but it was open-ended in how it could be approached. I enjoyed exploring varying strategies, weighing their costs in resources and potential benefits. Being completed during COVID was a challenge (especially when physical hardware was involved), but I believe it improved my ability to collaborate and communicate across teams.