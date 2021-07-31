# Bin_projet
This package will display the state of connected smart bins. There will be 4 state for the bin:
* state 0 : empty & light
* state 1 : full & heavy
* state 2 : empty & heavy
* state 3 : full & light

The objective is to inform the admin of the above state. 

## To install the package
Clone the repertory into the src folder in your catkin workspace

```sh
cd ~/catkin_ws/src
git clone https://github.com/henna19/bin_projet.git
catkin build
source ~/catkin_ws/devel/setup.bash
```

## TO run the package
### roscore

First of all you need to run the server. To do so open a terminal and run the following code:

```sh 
roscore
```

Don't forget to give execution rights to every files before executing them:
```sh 
chmod +x file_name.py
```
### rosrun
Then open another terminal in the package you cloned and run the following code:

```sh
cd catkin_ws
cd src/bin_project
cd src
rosrun bin_projet bin_server.py
```

### rostopic
Then run this code:
```sh
rostopic echo /bin_state
``` 
