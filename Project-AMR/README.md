Autonomous Mobile Robots (AMRs) rely on 3D LiDAR to navigate dynamic, human-shared indoor environments.
LiDAR sensors have a physical minimum detection range which increases the risk of collisions with near-field humans.
In our case, the AMR had a blind zone of about 70 cm. Humans within this zone are not detected and therefore not avoided.

Our solution to this near-field blind zone was to utilize a cooperative perception framework implemented in ROS 2 using machine-to-machine communication to bridge data from an overhead ceiling-mounted LiDAR
to the AMR's LiDAR.

This solution provides a real-time perception layer for active human detection, solving the blind zone issue without the need for modifications to the vehicle itself.

AMR:
<img width="3300" height="2475" alt="image13" src="https://github.com/user-attachments/assets/906afe3c-6c48-4da9-9d6c-b0c2d447a9aa" width="60" />

Overhead LiDAR:
<img width="2178" height="2112" alt="image12" src="https://github.com/user-attachments/assets/19355158-ebb9-48af-80e4-d0bffe0a43c6" width="60" />


Without human detection: The human steps into the AMR's physical blind zone from around a corner and does not react.  
<video src="https://github.com/user-attachments/assets/e0fadb18-65a8-44f1-8de0-965af270f90e" controls width="100%">
  Your browser does not support the video tag.
</video>

With human detection: The human steps into the AMR's blind zone and stops accordingly to replan its path.  
<video src="https://github.com/user-attachments/assets/896a6483-9ca3-4b7d-b24e-7ee4bcadaeba" controls width="100%">
  Your browser does not support the video tag.
</video>

AMR's LiDAR point cloud without human detection. Blind zone appears empty.
![Without human detection](./lidar-without-detection.jpg)

LiDAR point cloud with human detection. Human highlighted in red appears in the blind zone.
![With human detection](./lidar-with-detection.jpg)


