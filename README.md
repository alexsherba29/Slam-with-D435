# Slam-with-D435
Slam-with-D435 on jetson nano Presentation 
 
## installtion 
1) Install Swapfile
```bash
cd Slam-with-D435
./installSwapfile.sh
reboot
```
2) Install Librealsense library 
```bash
cd Slam-with-D435
./installDependencies.sh
./installLibrealsense.sh
./buildLibrealsense.sh
```
3) Run realsense-viewer
```bush
realsense-viewer
```
4) Python script with d435 for test
```python
python align-depth2color.py
python opencv_pointcloud_viewer.py
```
4) Install ROS on Jetson Nano
```bash 
./installROS.sh -p ros-melodic-desktop-full
./setupCatkinWorkspace.sh
./installRealSenseROS.sh
```
5) Install components
```bash
sudo apt-get install ros-melodic-imu-filter-madgwick
sudo apt-get install ros-melodic-rtabmap-ros
sudo apt-get install ros-melodic-robot-localization
```
## Usage 1

### in terminal 1
```bash
roscore
```
### in terminal 2
```bash
rviz
```
### in terminal 3
```bash
cd catkin_ws
source devel/setup.bash
roslaunch realsense2_camera rs_camera.launch
```
## Usage 2

### in terminal 1
```bash
roscore
```
### in terminal 2
```bash
roslaunch realsense2_camera opensource_tracking.launch
```

### License
[MIT](https://choosealicense.com/licenses/mit/)
