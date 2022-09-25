# UDEV Rules

```
sudo apt update
sudo apt install nano
```

`sudo nano /etc/udev/rules.d/99-vesc.rules`

`KERNEL=="ttyACM[0-9]*", ACTION=="add", ATTRS{idVendor}=="0483", ATTRS{idProduct}=="5740", MODE="0666", GROUP="dialout", SYMLINK+="sensors/vesc"`

`sudo nano /etc/udev/rules.d/99-ydlidar.rules`

`KERNEL=="ttyUSB[0-9]*", ACTION=="add", ATTRS{idVendor}=="10c4", ATTRS{idProduct}=="ea60", MODE="0666", GROUP="dialout", SYMLINK+="/sensors/ydlidar"`

`sudo nano /etc/udev/rules.d/99-joypad-f710.rules`

`KERNEL=="js[0-9]*", ACTION=="add", ATTRS{idVendor}=="046d", ATTRS{idProduct}=="c21f", SYMLINK+="input/joypad-f710"`

```
sudo udevadm control --reload-rules
sudo udevadm trigger
```

Reboot the system.

# ROS 2 Topics

```
git clone https://github.com/ros-perception/image_common.git --branch ros2
cd image_common
git reset --hard a62ab876da2599627fe6a86bbc79040c62509422 # Reset to Release Tag: 3.0.0
cd ~/zed_ros2_ws/
colcon build --symlink-install
source install/setup.bash
```

## Sensor Topics Published

/scan

vesc/odom
vesc/drive AckermannDriveStamped

/zed2/zed_node/rgb/image_rect_color
/zed2/zed_node/point_cloud/cloud_registered
/zed2/zed_node/obj_det/objects
/zed2/zed_node/imu/data
/zed2/zed_node/imu/mag
/zed2/zed_node/atm_press
/zed2/zed_node/pose
/zed2/zed_node/path_map
/zed2/zed_node/path_odom



## 
