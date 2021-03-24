[![Gentlebots.](http://gentlebots.gsyc.urjc.es/img/team.jpg)](http://gentlebots.gsyc.urjc.es/)
Gentlebots team is composed of two universities and is focused on software development that allows robots to exhibit intelligent behaviors. For this reason, the majority of the participations in competitions have been in leagues whose robot is standard for all the participants of the league, where the focus is in the programming of the algorithms. 

# Table of Contents
1. [TIAGo in Robocup2021 world. A LXD Container](https://github.com/gentlebots/gb_robots)

# Interesting links
[Robocup@Home challenge site](https://athome.robocup.org/home-virtual-2021/)

# Last Roadmap
Download [here](https://github.com/gentlebots/gentlebots/raw/main/content/RoadmapRobocup2021.pdf) the current Gentlebots Robocup2021 roadmap.

# Robocup2021 Rulebook
- [1st Draft](https://okdhryk.github.io/robocup2020dspl-sumulation/Rulebook.pdf)

# Gentlebots Ecosystem

## Steps
Install ROS2 Foxy from packages following the official [guide](https://docs.ros.org/en/foxy/Installation/Linux-Install-Debians.html), and [development tools](https://docs.ros.org/en/foxy/Installation/Linux-Development-Setup.html#install-development-tools-and-ros-tools).


Install nav2 from packages.
```
sudo apt-get install ros-foxy-nav2-*
sudo apt-get install ros-foxy-turtlebot3*
```

Create your robocup_ws, import our repos and compile it.
```
source /opt/ros/foxy/setup.bash
mkdir -p ~/robocup_ws/src
cd ~/robocup_ws/src
wget https://raw.githubusercontent.com/gentlebots/gentlebots/main/gentlebots.repos
vcs import < gentlebots.repos
cd ..
rosdep install -y -r -q --from-paths src --ignore-src --rosdistro foxy
colcon build --symlink-install
```
