# Objective #
1. Build a single floor wall structure using the Building Editor tool in Gazebo. Apply at least one feature, one color, and optionally one texture to your structure. Make sure there's enough space between the walls for a robot to navigate.
2. Model any object of your choice using the Model Editor tool in Gazebo. Your model links should be connected with joints.
3. Import your structure and two instances of your model inside an empty Gazebo World.
4. Import at least one model from the Gazebo online library and implement it in your existing Gazebo world.
5. Write a C++ World Plugin to interact with your world. Your code should display “Welcome to ’s World!” message as soon as you launch the Gazebo world file.




# Project Structure #
```
.Build-My-World                    # Build My World Project 
├── model                          # Model files 
│   ├── gokart
│   │   ├── model.config
│   │   ├── model.sdf
│   ├── myfloorplan
│   │   ├── model.config
│   │   ├── model.sdf
│   ├── robot
│   │   ├── model.config
│   │   ├── model.sdf
├── script                         # Gazebo World plugin C++ script      
│   ├── welcome.cpp
├── world                          # Gazebo main World containing models 
│   ├── myoffice.world
├── CMakeLists.txt                 # Link libraries 
└──   
```
# BUILD AND RUN #
1. Clone the repository 
2. create a Build directory
```
mkdir build && cd build
```
3. In ``` /build ```
```
cmake .. && make
```
4. Export the plugin folder
```
export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/RoboND-Term1-P1-Build-My-World/build
```
5. Launch Gazebo
```
cd /home/workspace/github/myrobot/world/
gazebo myworld.world
```
