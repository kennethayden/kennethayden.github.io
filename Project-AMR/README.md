Autonomous Mobile Robots (AMRs) rely on 3D LiDAR to navigate dynamic, human-shared indoor environments.
LiDAR sensors have a physical minimum detection range which increases the risk of collisions with near-field humans.
In our case, the AMR had a blind zone of about 70 cm. Humans within this zone are not detected and therefore not avoided.

Our solution to this near-field blind zone was to utilize a cooperative perception framework implemented in ROS 2 using machine-to-machine communication to bridge data from an overhead ceiling-mounted LiDAR
to the AMR's LiDAR.

This solution provides a real-time perception layer for active human detection, solving the blind zone issue without the need for modifications to the vehicle itself.

Without human detection: The human steps into the AMR's physical blind zone from around a corner and does not react.  
![Without human detection](./without-detection.gif)

With human detection: The human steps into the AMR's blind zone and stops accordingly to replan its path.  
![With human detection](./with-detection.gif)

AMR's LiDAR point cloud without human detection. Blind zone appears empty.
![Without human detection](./lidar-without-detection.jpg)

LiDAR point cloud with human detection. Human highlighted in red appears in the blind zone.
![With human detection](./lidar-with-detection.jpg)
