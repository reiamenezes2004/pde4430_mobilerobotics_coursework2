Launch files for gazebo, some model files and nodes for the assessment.

To get the best results it is important to update the version of gazebo installed.

Ensure you virtual machines ethernet connection is active, and you computer has an internet connection and then run these commands one after the other in a terminal window.

sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'

wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -

sudo apt-get update

sudo apt-get install gazebo7 -y

If you have issues with any of the turtlebot3 examples then clone the turtlebot3 packages into your workspace and build them along with your other packages.

To launch the base simulator simulator use

roslaunch assessment_world assessment_world.launch

to add the spheres and walls launch

roslaunch assessment_world objects.launch

To run it without launch the gui for gazebo use the original command, but add the parameter gui:=false

roslaunch assessment_world assessment_world.launch gui:=false

You will also need to run the command to add the other objects, but you do not need to change that command a gazebo has already been launched without its gui

If you want to run the simulation with a turtlebot3, to see what a robot looks like in the simulation and to see how you might control it then you can launch

roslaunch turtlebot3_gazebo turtlebot3_world.launch

and then run the objects launchfile to add the spheres and walls

