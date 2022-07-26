# Go Chase It

Ball chaser mobile robot using ROS and Gazebo.

This repo consists of two packages:
* `my_robot` package defines the simulation world and the robot.
* `ball_chaser` package contains the nodes responsible for controlling the robot.

## Prerequisites
* ROS installed on Linux
* Cmake
* gcc/g++ compiler

## Build
* Create and build a catkin workspace. If you have catkin_ws, skip to the next step.
    ```
    $ mkdir -p ~/catkin_ws/src
    $ cd /carkin_ws/src
    $ catkin_init_workspace
    $ cd /catkin_ws/
    $ catkin_make
    ```
* Clone the repository to your source folder.
    ```
    $ cd /catkin_ws/src
    $ git clone https://github.com/yabdulra/Go-Chase-It.git
    $ cd ..
    $ catkin_make
## Launch
* Launch the simulation world
    ```
    $ source devel/setup.bash
    $ roslaunch my_robot world.launch
    ```
* In a new terminal, launch the `ball_chaser` package.
    ```
    $ source devel/setup.bash
    $ roslaunch ball_chaser ball_chaser.launch
    ```
Now that everything is set, pickup the white ball and place it within the field of view of the robot. The robot will follow the white ball.

https://user-images.githubusercontent.com/61895971/180902896-4ab51830-9e53-4ad9-9793-05fe87f84c00.mp4