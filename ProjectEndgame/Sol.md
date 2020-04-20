My solution on the problem.

These are the sensor inputs that need to be used. 

Name   Range(Unit)

ob.angle    [-pi,pi]

ob.track    (0,200)(meters)

ob.trackPos     (−inf,inf)

ob.speedX       (−inf,inf)(km/h)

ob.speedY        (−inf,inf)(km/h)



Angle would help know the steering angle for the car

the track would tell where on the the given road is the car

trackPos will tell how far away from the destination the car is

speedX,speedY will be the 2 velocities in the 2 directions.

I need to modify my rewards equation. TO make it work. I was thinking in terms of velocity along the speed of the path must be punished when the agent deviates from the center of the road.

after sometime the code does break. There's an error in the kivy file. I need to figure it out.

The model is training okay. But the output is not vey convincing. need to work on the rewards equation.





IN THE UPCOMING TIME -> 

I want to test like you said yesterday. First train on without the map. And second time train with a map and no destination. After that should we use ensemble? Probably not. the code might break. xD , need to figure out how that goes.

I read upon online, they've implemented with TORCS environment, the First person movement of car in traffic, I'm trying to gain some insights from that code.




