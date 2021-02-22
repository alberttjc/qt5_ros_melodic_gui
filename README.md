# A User Interface Package Template for ROS Melodic based on Qt5 Widgets

![GUI](resources/images/gui.png?raw=true "GUI")

## Create WS

```
# if the belowd does not work, do sudo pip3 install git+https://github.com/catkin/catkin_tools.git first
mkdir -p <workspace_name>/src
cd <workspace_name>/src
git clone https://github.com/catkin/catkin_simple.git
cd catkin_simple
mkdir build
cd build
cmake ..
make
cd <workspace_name>
catkin init
catkin config --merge-devel # Necessary for catkin_tools >= 0.4.
catkin config --extend /opt/ros/$ROS_DISTRO
catkin config --cmake-args -DCMAKE_BUILD_TYPE=Release
```

## Install dependencies

Qt 5 independent of ROS:

```
sudo apt-get install qtbase5-dev
```

```
wstool init
wstool merge nav/nav_ui/dependencies.rosinstall # might not work
wstool update
```
