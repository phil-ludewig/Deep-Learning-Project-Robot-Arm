# Deep Learning Project Robot Arm
This project demonstrates the application of a Deep Reinforcement Learning agent on a simulated picking task.

#### Full Project Writeup
[Writeup PDF](http://pioneerlabs.de/wp-content/uploads/2019/04/DeepRL-Arm-Writeup.pdf)

#### Video of the learning process:
https://www.youtube.com/watch?v=riRW5Fx_iV4

#### Main Work
The main task here consisted of building the [Gazebo Plugin](https://github.com/phil-ludewig/Deep-Learning-Project-Robot-Arm/blob/master/gazebo/ArmPlugin.cpp):
* Defining Input and Output of DQN Agent
* Tuning of DQN Hyperparameters
* Building Reward Functions & Agent Actions
* Interfacing with ROS topics

## Abstract
This project is based on the Nvidia open source example "jetson-reinforcement" developed by Dustin Franklin. The objective is to integrate a deep reinforcement agent with a robotic arm in a simulated Gazebo environment. By defining reward functions and deep learning parameters, the Deep RL agent incrementally learns the goal of moving towards an object to touch it.

## Results
#### Environment Overview:
![Overview](results/Images/Arm.jpg "ALT")

#### RAW Camera DQ-Network Input:
![RAWCamera](results/Images/CameraInput.jpg "ALT")

#### 90% Accuracy in Touching the Object ():
![Progress](results/Images/Task1_TouchAny_BaseLocked_90%.png "ALT")
