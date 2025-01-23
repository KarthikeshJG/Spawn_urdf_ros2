---

# Spawn URDF in ROS 2 with Rviz

This repository provides a simple setup to check your URDF files in ROS 2 using Rviz. Follow the steps below to clone, modify, and launch your URDF file visualization.

---

## Repository Link

[Spawn_urdf_ros2](https://github.com/KarthikeshJG/Spawn_urdf_ros2)

---

## Prerequisites

Ensure you have the following installed:
- **ROS 2** (Humble or any compatible distribution)
- Rviz2
- Colcon build tools

---

## Steps to Use

### 1. Clone the Repository
Clone this repository into your ROS 2 workspace:
```bash
cd ~/ros2_ws/src
git clone https://github.com/KarthikeshJG/spawn_urdf_ros2.git
```

---

### 2. Add Your URDF File
Place your URDF file in the `urdf` folder of this repository:
```bash
cd ~/ros2_ws/src/spawn_urdf_ros2/urdf
cp <your-urdf-file>.urdf .
```

---

### 3. Modify the Launch File
Update the launch file to reference your URDF file:
1. Open `urdf.launch.py` in a text editor:
   ```bash
   nano ~/ros2_ws/src/spawn_urdf_ros2/launch/urdf.launch.py
   ```
2. Locate **Line 32** and replace the URDF file name with the name of your URDF file:
   ```python
   urdf_file_name = 'your_urdf_file.urdf'
   ```

---

### 4. Build the Workspace
Build your ROS 2 workspace to ensure everything is set up:
```bash
cd ~/ros2_ws
colcon build
source install/setup.bash
```

---

### 5. Launch the URDF in Rviz
Launch the setup to visualize your URDF:
```bash
ros2 launch spawn_urdf_ros2 urdf.launch.py
```

---

## Expected Output
- Rviz2 will launch, and your URDF model should be visible.
- Verify that all links, joints, and visuals appear as expected.

---

## Troubleshooting
1. **Missing URDF file error**: Ensure the URDF file name is correctly specified in the launch file.
2. **Rviz not showing model**: Check for syntax errors in your URDF file and confirm that all required meshes are accessible.

---

## License
This repository is licensed under the MIT License. See the LICENSE file for more details.

---

