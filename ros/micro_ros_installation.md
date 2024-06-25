# MicroRos installation

For the installation of MicroRos, we will use the `ros2` command line tool. If you don't have it installed, you can follow the instructions [here](https://docs.ros.org/en/humble/Installation.html) and make sure to choose the right ROS 2 distribution for your system and follow the instructions for your OS, I will be using `ROS 2 Humble Hawksbill`.

## Installation _[(Official Summary)](https://micro.ros.org/docs/tutorials/core/first_application_linux/)_

1. First, we need to add the MicroRos repository to the ROS 2 workspace. To do this, we will use the `ros2` command line tool. Run the following command:
    * Create a new workspace in the location of your choice:

    ```bash
    mkdir -p micro_ros_ws
    cd micro_ros_ws
    ```

    * Source ROS2 installation:

    ```bash
    source /opt/ros/humble/setup.zsh # or .bash if you are using bash
    ```

    * Add the MicroRos repository to the workspace:

    ```bash
    git clone -b $ROS_DISTRO https://github.com/micro-ROS/micro_ros_setup.git src/micro_ros_setup
    ```

    * Update the system packages, rosdep, and install dependencies and make sure you have pip3 installed:

    ```bash
    sudo apt-get update && rosdep update
    rosdep install --from-paths src --ignore-src -r -y
    sudo apt-get install python3-pip
    ```

    * Build the workspace and source it:

    ```bash
    colcon build
    source install/local_setup.zsh # or .bash if you are using bash
    ```

    **Note**
    * up to this point, you have installed the MicroRos build system.
