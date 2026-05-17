Autonomous Mobile Robots (AMRs) rely on 3D LiDAR to navigate dynamic, human-shared indoor environments.
LiDAR sensors have a physical minimum detection range which increases the risk of collisions with near-field humans.
In our case, the AMR had a blind zone of about 70 cm. Humans within this zone are not detected and therefore not avoided.

Our solution to this near-field blind zone was to utilize a cooperative perception framework implemented in ROS 2 using machine-to-machine communication to bridge data from an overhead ceiling-mounted LiDAR
to the AMR's LiDAR.

This solution provides a real-time perception layer for active human detection, solving the blind zone issue without the need for modifications to the vehicle itself.

### Overview
<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>AMR:</h4>
      <img alt="image13" src="https://github.com/user-attachments/assets/906afe3c-6c48-4da9-9d6c-b0c2d447a9aa" width="100%" />
    </td>
    
  <td width="50%" valign="top">
      <h4>Overhead LiDAR:</h4>
      <img alt="image12" src="https://github.com/user-attachments/assets/19355158-ebb9-48af-80e4-d0bffe0a43c6" width="100%" />
    </td>
  </tr>
</table>

### Behavior Comparison

Without human detection: The human steps into the AMR's physical blind zone from around a corner and does not react.  
<video src="https://github.com/user-attachments/assets/e0fadb18-65a8-44f1-8de0-965af270f90e" controls width="100%">
  Your browser does not support the video tag.
</video>

With human detection: The human steps into the AMR's blind zone and stops accordingly to replan its path.  
<video src="https://github.com/user-attachments/assets/896a6483-9ca3-4b7d-b24e-7ee4bcadaeba" controls width="100%">
  Your browser does not support the video tag.
</video>

### Point Cloud Detection
<table width="100%">
  <tr>
    <td width="33.33%" valign="top">
      <br><br> <img alt="image15" src="https://github.com/user-attachments/assets/bca4c310-a1ee-42a4-9cc8-576966197417" width="100%" />
    </td>

  <td width="33.33%" valign="top">
      <h4>Without human detection:</h4>
      <p>Blind zone appears empty.</p>
      <img alt="image16" src="https://github.com/user-attachments/assets/e036ad80-e98d-46f2-aa28-ebd282a7e73c" width="100%" />
    </td>
    
  <td width="33.33%" valign="top">
      <h4>With human detection:</h4>
      <p>Human highlighted in red appears in the blind zone.</p>
      <img alt="image17" src="https://github.com/user-attachments/assets/a666a945-3fb3-46f6-8a1c-a7f5a4180696" width="100%" />
    </td>
  </tr>
</table>



