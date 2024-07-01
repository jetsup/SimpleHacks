# Micro-ROS Agent

The Micro-ROS Agent is a tool that allows you to interact with the Micro-ROS ecosystem. It is a bridge between the ROS 2 world and the Micro-ROS world. The agent is responsible for managing the communication between the ROS 2 world and the Micro-ROS world. It is a key component in the Micro-ROS architecture.

## Installation

To install the Micro-ROS Agent, you need to follow the steps below:

1. First, you need to add the Micro-ROS repository to the ROS 2 workspace. To do this, you will use the `ros2` command line tool. Run the following command:

    ```bash
    mkdir -p micro_ros_ws
    cd micro_ros_ws
    source /opt/ros/humble/setup.zsh # or .bash if you are using bash
    git clone -b $ROS_DISTRO https://github.com/micro-ROS/micro_ros_setup.git src/micro_ros_setup
    sudo apt-get update && rosdep update
    rosdep install --from-paths src --ignore-src -r -y
    sudo apt-get install python3-pip
    colcon build
    source install/local_setup.zsh # or .bash if you are using bash
    ```

2. Once you have installed the Micro-ROS build system, you can install the Micro-ROS Agent. To do this, run the following command:

    ```bash
    ros2 run micro_ros_setup create_agent_ws.sh
    ```

3. After running the command, you will need to build the agent so that it can be used. To build the agent, run the following command:

    ```bash
    ros2 run micro_ros_setup build_agent.sh
    ```

4. Once you have built the agent, you can run it using the following command:

    ```bash
    ros2 run micro_ros_agent micro_ros_agent udp4 --port [PORT NUMBER] # if you are using a UDP connection
    ```

    or

    ```bash
    ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/ttyACM0 # if you are using a serial connection
    ```
