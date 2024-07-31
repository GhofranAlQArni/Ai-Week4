# Ai-Week4
running and navigation with Turtelbot3

# Table of Contents:

1- Install turthbox3 
2- Set model 
3-Launch Simulation World
4- Run Navigation Node
5- Set Navigation Goal



![Gh-Ai](https://github.com/user-attachments/assets/2752997d-f745-4520-b9be-a857bb7cb2d3)




# ____________________________________________________________________________________________________________________________________________________________________________________________






Here explains the process of setting up and using the TurtleBot3 robot for navigation tasks in a simulated environment using ROS Noetic. It includes instructions for installing necessary packages, configuring the TurtleBot3 model, launching the simulation in Gazebo, creating a map using SLAM, to be able to effectively control the TurtleBot3, generate a map of your environment.

 # to installing TURTLEBOT3 :

```
sudo apt install ros-noetic-turtlebot3
sudo apt install ros-noetic-turtlebot3-simulations
sudo apt install ros-noetic-turtlebot3-navigation
sudo apt-get install ros-noetic-dwa-local-planner
```


# To set the model : 

```
echo "export TURTLEBOT3_MODEL=waffle" >> ~/.bashrc
source ~/.bashrc
```


# Launch-Simulation-World
Navigation is to move the robot from one location to the specified destination in a given environment. For this purpose, a map that contains geometry information of furniture, objects, and walls of the given environment is required. As described in the previous SLAM section, the map was created with the distance information obtained by the sensor and the pose information of the robot itself.

Please use the proper keyword among burger , waffle , waffle_pi for the TURTLEBOT3_MODEL parameter.


```
$ export TURTLEBOT3_MODEL=waffle

$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

<img width="614" alt="image" src="https://github.com/user-attachments/assets/75a0386d-0ecb-44ab-8b9a-54808d4e1eab">



# Run-Navigation-Node
Open a new terminal from Remote PC with Ctrl + Alt + T and run the Navigation node.
Please use the proper keyword among burger , waffle , waffle_pi for the TURTLEBOT3_MODEL parameter.

```
$ export TURTLEBOT3_MODEL=waffle

$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```


![Screenshot 2024-07-31 191123](https://github.com/user-attachments/assets/5d3dabfb-5490-4e3d-a120-0dec3cfbab4d)


# Set-Navigation-Goal
Click the 2D Nav Goal button in the RViz menu. Click on the map to set the destination of the robot and drag the green arrow toward the direction where the robot will be facing

<img width="638" alt="image" src="https://github.com/user-attachments/assets/7b428d65-6ae8-4c27-82ca-c71877cf6d65">





