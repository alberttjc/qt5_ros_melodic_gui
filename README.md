# qt5_ros_melodic_gui


![GUI](resources/images/gui.png?raw=true "GUI")

## Introduction

A User Interface Package Template for ROS Melodic based on Qt5 Widgets

## Install dependencies

```
# Qt 5 dependencies of ROS:
$ sudo apt-get install qtbase5-dev

# To install Qt creator
$ sudo apt-get install qtcreator
```

## Setup

Before you can use this repository, you need to install [catkin_simple](https://github.com/catkin/catkin_simple.git) first.

```
# if the belowd does not work, do sudo pip3 install git+https://github.com/catkin/catkin_tools.git first
$ mkdir -p <workspace_name>/src
$ cd <workspace_name>/src
$ git clone https://github.com/catkin/catkin_simple.git
$ cd catkin_simple
$ mkdir build
$ cd build
$ cmake ..
$ make
$ cd <workspace_name>
$ catkin init
$ catkin config --merge-devel # Necessary for catkin_tools >= 0.4.
$ catkin config --extend /opt/ros/$ROS_DISTRO
$ catkin config --cmake-args -DCMAKE_BUILD_TYPE=Release

# Once it is all configured
$ cd <workspace_name>/src
$ git clone https://github.com/alberttjc/qt5_ros_melodic_gui.git
$ wstool init
$ wstool merge nav/nav_ui/dependencies.rosinstall # might not work
$ wstool update
```
