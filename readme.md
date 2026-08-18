## 1. Prerequisites
### 1.1 **Ubuntu** and **ROS2**
Ubuntu 64-bit 22.04.
ROS Humble. [ROS2 Installation](https://docs.ros.org/en/humble/)

### 1.2. **serial**
~~~
git clone https://github.com/RoverRobotics-forks/serial-ros2.git
cd serial-ros2
mkdir build && cd build
cmake ..
make -j$(nproc)
sudo make install
~~~

### 1.3. **eigen**
sudo apt-get install libeigen3-dev

## 2. Build
在工作空间文件夹中：
终端输入：
~~~
colcon build --packages-select quadrotor_msgs
source install/setup.bash
colcon build
~~~

## 3. Source
source install/setup.bash

## 4. 如果用到串口需要配置权限
sudo chmod 777 /dev/ttyACM0

## 5. 运行launch文件
ros2 launch fcu_core fcu_core_launch.py