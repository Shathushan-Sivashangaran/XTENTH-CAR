# ROS 2 Workspace

## Dependencies

```
git clone https://github.com/ros-perception/image_common.git --branch ros2
cd image_common
git reset --hard a62ab876da2599627fe6a86bbc79040c62509422 # Reset to Release Tag: 3.0.0
cd ~/zed_ros2_ws/
colcon build --symlink-install
source install/setup.bash
```

## UDEV Rules

XTENTH-CAR requires knowledge of device names assigned by the operating system for VESC, YDLIDAR G2 and F710 Wireless Gamepad. These names can vary each time the Jetson SOM is rebooted. To assign persistent device names, use the udev utility. 

1. Install the GNU nano text editor.

```
sudo apt update
sudo apt install nano
```

2. Assign VESC the name `/dev/sensors/vesc`.

`sudo nano /etc/udev/rules.d/99-vesc.rules`

Copy `KERNEL=="ttyACM[0-9]*", ACTION=="add", ATTRS{idVendor}=="0483", ATTRS{idProduct}=="5740", MODE="0666", GROUP="dialout", SYMLINK+="sensors/vesc"` in a single line and save the file.

3. Assign YDLIDAR G2 the name `/dev/sensors/ydlidar`.

`sudo nano /etc/udev/rules.d/99-ydlidar.rules` 

Copy `KERNEL=="ttyUSB[0-9]*", ACTION=="add", ATTRS{idVendor}=="10c4", ATTRS{idProduct}=="ea60", MODE="0666", GROUP="dialout", SYMLINK+="/sensors/ydlidar"` in a single line and save the file.

4. Assign F710 Wireless Gamepad the name `/dev/input/joypad-f710`.

`sudo nano /etc/udev/rules.d/99-joypad-f710.rules`

Copy `KERNEL=="js[0-9]*", ACTION=="add", ATTRS{idVendor}=="046d", ATTRS{idProduct}=="c21f", SYMLINK+="input/joypad-f710"` in a single line and save the file.

5. Activate the rules.

```
sudo udevadm control --reload-rules
sudo udevadm trigger
```

6. Reboot the system.

## Topics

`/zed2/zed_node/rgb/image_rect_color`

`/zed2/zed_node/point_cloud/cloud_registered`

`/zed2/zed_node/obj_det/objects`

`/zed2/zed_node/imu/data`

`/zed2/zed_node/imu/mag`

`/zed2/zed_node/atm_press`

`/zed2/zed_node/pose`

`/zed2/zed_node/path_map`

`/zed2/zed_node/path_odom`

`/scan`

`vesc/odom`

`vesc/drive AckermannDriveStamped`



