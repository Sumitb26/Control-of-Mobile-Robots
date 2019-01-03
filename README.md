# Control of Mobile Robots
Control of Mobile Robots is a course that focuses on the application of modern control theory to the problem of making robots move around in safe and effective ways.

### Week 1 - Introduction to Robots
- Learn about MATLAB and the robot simulator

### Week 2 - Mobile Robots
- Implement the transformation from unicycle dynamics to differential drive dynamics
- Implement odometry for the robot
- Implement code that converts raw IR values to distances (in meters)

### Week 3 - Linear Systems
- Calculate the heading (angle), &theta;<sub>g</sub>,  to the goal location (x<sub>g</sub>,y<sub>g</sub>)
- Calculate the error between &theta;<sub>g</sub>  and the current heading of the robot, &theta;
- Calculate the proportional, integral, and derivative terms for the PID regulator that steers the robot to the goal.

### Week 4 - Control Design
- Transform the IR distance measured by each sensor to a point in the reference frame of the robot
- Transform the point in the robot's reference frame to the world's reference frame
- Use the set of transformed points to compute a vector that points away from the obstacle

### Week 5 - Hybrid Systems
- Combine go-to-goal controller and avoid-obstacle controller into a single controller that blends the two behaviors
- Implement the switching logic that switches between the go-to-goal controller and the avoid-obstacles controller
- Improve the switching arbitration by using the blended controller as an intermediary between the go-to-goal and avoid-obstacles controller

### Week 6 - The Navigation Problem
- Compute a vector, &mu;<sub>f&omega;,t</sub>, that estimates a section of the obstacle ("wall") next to the robot using the robot's right (or left) IR sensors
- Compute a vector, &mu;<sub>f&omega;,p</sub>, that points from the robot to the closest point on &mu;<sub>f&omega;,t</sub>
- Combine the two vectors, such that it can be used as a heading vector for a PID controller
### Week 7 - Putting It All Together
- Implement the progress_made event that will determine whether the robot is making any progress towards the goal
- Implement the sliding_left and sliding_right events that will serve as a criterion for whether the robot should continue to follow the wall (left or right) or switch back to the go-to-goal behavior
- Implement the finite state machine that will navigate the robot to the goal located without colliding with any of the obstacles in the environment
