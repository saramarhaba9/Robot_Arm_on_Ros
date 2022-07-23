# Robot_Arm_on_Ros



On Ubuntu, you should first install ROS; if you haven't done so, follow the instructions at https://github.com/saramarhaba9/ROS-installation-/blob/main/README.md


# Git the Robot Arm Package form Smart Methods 

on the Terminal: 

          source /opt/ros/noetic/setup.bash
          
          mkdir -p ~/catkin_ws/src
          
          cd ~/catkin_ws/
          
          catkin_make
          
          echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
          
          source ~/.bashrc      
          
          cd ~/catkin_ws/src
          
          sudo apt install git
          
          git clone https://github.com/smart-methods/arduino_robot_arm.git
          
          
       
      
# Install dependencies 

          cd ~/catkin_ws

          rosdep install --from-paths src --ignore-src -r -y

          sudo apt-get install ros-noetic-moveit

          sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

          sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

          sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

          sudo nano ~/.bashrc


add the following line to bashrc's end:

          source /home/(your Ubuntu OS name) /catkin_ws/devel/setup.bash
 
Press: 

      ctrl + o 

      Enter 

      ctrl + x 


Then write the following command on Terminal: 
          
          catkin_make
          roslaunch robot_arm_pkg check_motors.launch
          
Now the RIVZ has opened, you can observe a robot arm simulation.

![Rivz ](https://user-images.githubusercontent.com/56765097/180605347-fd1ab6f7-5dbd-44e1-9dee-7f665c7a37f1.png)


