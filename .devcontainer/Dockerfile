FROM ghcr.io/aica-technology/ros2-ws:v2.0.6-jazzy

USER root

RUN apt-get update && apt-get install -y \
  ros-$ROS_DISTRO-behaviortree-cpp-v3 \
  ros-$ROS_DISTRO-turtlesim

USER ros2

RUN git clone https://github.com/BehaviorTree/BehaviorTree.ROS2 /home/ros2/ws/src/btcpp

RUN rosdep update && rosdep install --from-paths /home/ros2/ws/src --ignore-src -y

