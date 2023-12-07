---
title: "Integrating a Novel Industrial Robot for Surgical Use"
excerpt: "<br/><img src='/images/mecademic-meca500-6-axis-robot-arm-png-4.png' width='500' height='500'>"
collection: projects
---

The ARMA Lab at Vanderbilt uses the [Meca500](https://www.mecademic.com/meca500-industrial-robot-arm/) industrial robot to assist in [ocular therapeutic delivery](http://arma.vuse.vanderbilt.edu/index.php/research?id=208). Using a mass-produced, small form factor, and extremely precise 6-arm robot has clear advantages when developing an aid to surgeons. **This was enabled by the groundwork I produced while researching, analyzing, and troubleshooting the robot for use in the lab.**

I investigated three fundamental questions to if this industrial robot is suitable for surgery:
* Can the response time of the robot be reduced to a level that is acceptable for critical surgeries?
* Can it be integrated into the existing lab tech stack?
* How confident can you be in using this robot near sensitive areas?

In testing, TCP/IP communication appeared to be hard coded near 15 ms, or 66 Hz, which is not enough for surgery. The Meca500 also supports EtherCAT, an exceptionally fast ethernet protocol that guarantees a 2 ms response time. However, this is where the project faced a significant challenge. As a product that came to market recently, it had a stark lack of documentation, particularly for using EtherCAT with any of the languages already used in the lab (C++, Python, Matlab/Simulink Real-Time).

Through research, communication with Mecademic, and a large amount of trial and error, I successfully developed Python scripts using EtherCAT while creating ground-up documentation for the rest of the team to build on for their surgical applications. This **reduced round-trip latency from 50 to 2 ms** and allowed for easy integration into existing lab protocols, answering the first two questions.

This left the final, and perhaps most important question of whether the robot can be used safely around patients. While the robot boasts a positional repeatability of 0.005mm, how it gets to the target position is extremely important. For example, if you command the robot to hold a needle 2mm away from the patient’s eye, you generally want it to get there without going through the patient or their eye. Notably, there is a “blending” parameter that aims to make movements smoother and less discrete at the cost of not knowing the exact path taken toward the end position. After careful analysis and tests, I determined blending should be used with caution, and that small, extremely precise steps in movement were key in creating predictable movement necessary for highly sensitive tasks. This answered the third question, allowing the ARMA lab to proceed with the robot for surgical applications.



<sup>Note: a Mecademic provided Python API exists now, and I would highly recommend it for future use. While a portion of my work is probably mirrored in what is provided there, the principal goal was to promptly determine if this robot was viable for a grant, and by that measure, I am quite satisfied.</sup>
