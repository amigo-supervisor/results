# results
This repository holds the results of implementing the case studies on the Amigo robot. 
Everyhting is implemented correctly on the supervisor side, but some extra functionality in the wrapper are still missing.
As of now the following is not yet implemented:

## collision checking
While the kinect sensor has been integrated in moveit and there is an action server reporting the validity of the path, it was not yet robust enough to use in the experiments

## Check for object bewlow hand
Since we need collision checking for this, this is also not implemented yet

## Arm choice
At time of the experiments one of the arms was broken, so there is no function yet that decides what arm to chose

## Hard coded waypoints and objects
CIF does not allow string variables, so the order of objects to grab and waypoints to navigate to is now hard coded in the wrapper.
This is somehting that needs to be looked in to.

## Move arm in direction of object
For the current experiments it was sufficient to just show that the arm can move, while the base is moving, so it is just moving to the carrying pose.
In the future it would be nice if the arm would move towards the object, when it sees it. 
This is not straightforward, however, because the way amigo works at the moment, we need to inspect an entity first to see what objects are on it.
