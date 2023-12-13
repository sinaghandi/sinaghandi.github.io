---
title: "Using Computer Vision for Robot Calibration"
excerpt: "<br/><img src='/images/pixycam_demo.jpg' width='500' height='500'>"
collection: projects
---
<figure style="width: 500px;">
    <img src='/images/annotated_pixycam.jpg'>
    <figcaption>The (1.) PixyCam on a prototype mount taking readings from (2.) colored felt markers on the robot's joints.</figcaption>
</figure>

This project transformed a tedious manual calibration process undertaken by every student in a robotics outreach program into a short, automatic session. Through the use of computer vision, I significantly reduced calibration time, introduced students to computer vision and optimization, and provided a platform for creative programming applications.

I researched and tested various solutions, settling on the PixyCam, a cheap and intuitive color-detecting camera. While a solution like OpenCV and a webcam may be more accurate, the main mission is to improve and expand on a project done by high schoolers, so keeping the software stack understandable and accessible was key. Using PixyCam allows us to use a straightforward combination of Arduino for robot/camera control and data collection and MATLAB for data storage and running an optimization algorithm. Simplifying the data acquisition process allows the students to focus on more important lessons in a limited amount of time.

Aside from enormous time improvement, this provides a natural next step for students in the robotics outreach program, exposing them to more advanced concepts and allowing them to imagine and program their own additions, such as visual servoing. As a high school intern, I faced a significant learning curve to contribute to the project, and I learned how to use my resources and the collaboration of my colleagues to the fullest. Despite the challenge, it was extremely rewarding to work towards increasing access to something both enriching and that I found enjoyable.

Key technical contributions included:
* Programmed MATLAB script simulating robot data (with error and noise) for testing
* Implemented a MATLAB calibration script utilizing the [Levenberg–Marquardt optimization algorithm](https://en.wikipedia.org/wiki/Levenberg%E2%80%93Marquardt_algorithm) to minimize residuals of loop closure equations
* Developed Arduino code to pose robot in various configurations and collect raw data from PixyCam
* Designed CAD model for centered camera mount above robot
