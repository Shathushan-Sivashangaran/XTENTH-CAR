# XTENTH-CAR
XTENTH-CAR (eXperimental one-TENTH scaled vehicle platform for Connected autonomy and All-terrain Research) aims to increase accessibility of experimental Connected Autonomous Vehicle (CAV) and Autonomous Ground Vehicle (AGV) research with low upfront costs, and complete Autonomous Vehicle (AV) hardware and software architectures, similar to the full-sized X-CAR experimental vehicle platform, enabling efficient cross-platform development between small-scale and full-scale vehicles [1], [2].

<p align="center">
<img src="https://github.com/Shathushan-Sivashangaran/XTENTH-CAR/blob/main/images/XTENTH-CAR_assembled.JPG" width="600">
</p>


## Hardware Build
The platform is equipped with the best-in-class NVIDIA Jetson AGX Orin System on Module (SOM), stereo camera with built-in Inertial Measurement Unit (IMU), barometer and magnetometer, 2D LiDAR and VESC, an open-source Electronic Speed Controller (ESC) with drivers written in the new Robot Operating System (ROS 2) to facilitate experimental CAV and AGV research that incorporate state-of-the-art computationally expensive algorithms such as Deep Reinforcement Learning. See [XTENTH-CAR/hardware](https://github.com/Shathushan-Sivashangaran/XTENTH-CAR/tree/main/hardware) for full Bill of Materials (BOM), CAD files and hardware assembly guide.


## Software Installation
NVIDIA Jetson series SOMs utilize the NVIDIA JetPack Software Development Kit (SDK) which includes bootloader, Linux kernel and Ubuntu desktop environment. XTENTH-CAR software is written using ROS 2 Foxy Fitzroy on JetPack v5+, which runs Ubuntu 20.04 natively.

1. See [NVIDIA JetPack SDK](https://docs.nvidia.com/jetson/jetpack/install-jetpack/index.html#package-management-tool) to install/upgrade JetPack components that include CUDA toolkit, cuDNN, TensorRT, OpenCV, NVIDIA container runtime with Docker integration, Multimedia API and NVSCI.

2. Install [ROS 2 Foxy Fitzroy](https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html), [colcon](https://docs.ros.org/en/foxy/Tutorials/Beginner-Client-Libraries/Colcon-Tutorial.html) and [rosdep](https://docs.ros.org/en/foxy/Tutorials/Intermediate/Rosdep.html) to build ROS 2 packages.

3. Clone the contents of [XTENTH-CAR/xtenthcar_ws/src](https://github.com/Shathushan-Sivashangaran/XTENTH-CAR/tree/main/xtenthcar_ws/src) into the src directory of a newly created ROS 2 workspace `xtenthcar_ws/src`.

4. See [XTENTH-CAR/xtenthcar_ws/README.md](https://github.com/Shathushan-Sivashangaran/XTENTH-CAR/blob/main/xtenthcar_ws/README.md) to install dependencies and create udev rules.

5. Build the workspace by running `colcon build` in the workspace root directory.


## Citations

For more information on XTENTH-CAR and full-size X-CAR refer to the following papers. Cite [1] if you used XTENTH-CAR in your research.

```
[1] S. Sivashangaran and A. Eskandarian, “XTENTH-CAR: A Proportionally Scaled Experimental Vehicle Platform for Connected Autonomy and All-Terrain Research,” arXiv preprint, 2022.

[2] G. Mehr, P. Ghorai, C. Zhang, A. Nayak, D. Patel, S. Sivashangaran, and A. Eskandarian, “X-CAR: An Experimental Vehicle Platform for Connected Autonomy Research,” IEEE Intelligent Transportation Systems Magazine, pp. 2–19, 2022.
```
