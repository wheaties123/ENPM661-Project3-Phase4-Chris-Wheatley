Chris Wheatley
University of Maryland (College Park)
ENPM661 Spring 2020
Dr. Monfaredi
Project #3 - Phase #4 - Scenario 1

Project Description:
Phase 4 of project 3 allows students to simulate (either in VREP or Gazebo) nonhalonomic differential-drive A* searching for a rigid robot.  The simulations generated in Phase 4 were derived from positions and wheel velocities generated in Phase 3.

Phase 4 of Project 3 contains the following folders: 
	- Scenario1 (shorter scenario / hemisphere around bottom-left circle)
		o map_world_shorterScenario.ttt
		o robot_child_script_shorterScenario.txt
		o simulation1_vrep_shorterScenario.mp4
	- Scenario2 (longer scenario / from bottom left to top right)
		o map_world_longerScenario.ttt
		o robot_child_script_longerScenario.txt
		o simulation2_vrep_longerScenario.mp4
	
Simulation Paramaters for Each Scenario (chosen at own discretion, as instructed by professor):
	- Scenario 1
		o Start Node: [-4,-3,90] 
		o Goal Node: [0,-3]
		o Clearance: 0.3
		o Wheel RPMs: [14, 5]
		o Hard-coded assumptions:
			-- Simulation stops when robot comes within a distance of 0.2 meters or less to the goal.
	- Scenario 2
		o Start Node: [-4,-3,90] 
		o Goal Node: [4,3]
		o Clearance: 0.35
		o Wheel RPMs: [14, 5]
		o Hard-coded assumptions:
			-- Simulation stops when robot comes within a distance of 0.45 meters or less to the goal.	
			
NOTES (please read and consider):
	- This was my first time ever using VREP or LUA.
	- I performed Project 3 Phase 4 using VREP.  I selected VREP since VREP is installed on my own machine, and, to my knowledge, there wasn't a way to set publish to a ROS node when I have ROS and Gazebo installed on a Virtual Machine.  I also have been programming all assignments using MATLAB.
	- In VREP, I manually recreated the world map (as instructed by professor), and then modified the non-threaded child script of the robot model based on the position and velocity outputs from Phase 3.
	- I used the Pioneer robot in VREP since I could not find a Turtlebot model, and this was the closest in dimension that I could find. 
	- The main MATLAB script in Phase 3 prints out some arrays (for waypoint loaction, orientation, and wheel velocities) to the MATLAB Command Window, which I then copy and pasted into lines 3-7 of the Pioneer child script.
	- I copied all text from the modified child scripts for each scenario and pasted them into the "robot_child_script..." .txt files.
	- In the simulation .mp4 videos I attached for each scenario, note that I show the MATLAB explored area and shortest path prior to running simulation.

Video (.mp4) files, showing the VREP simulations, are provided for both folders for Scenarios 1 and 2, respectively.

If you want to run the simulations in VREP yourself, please follow the steps below:

User Instructions To Run Simulations in VREP:
1)  Ensure that CoppeliaSim/VREP is installed on your machine.
2)  Download and unzip all Project 3 Phase 4 contents.
3)  For Scenario 1:
		a) Navigate to "Scenario1" folder.
		b) Open the "map_world_shorterScenario.ttt" file in VREP.
		c) Make sure the scene loads completely (map w/obstacles and Pioneer robot).
		d) In top ribbon, click the right-pointing arrow to start simulation.
		e) Once the robot reaches within the threshokd siatnce of the goal node, both motors will stop moving.
		f) Feel free to open up the "Pioneer_p3dx" non-threaded child script within the left menu / scene hierarchy.
			o Note that this I copied this script into the "robot_child_script_shorterScenario.txt" file in the attached "Scenario1" folder.

	For Scenario 2:
		a) Navigate to "Scenario2" folder.
		b) Open the "map_world_longerScenario.ttt" file in VREP.
		c) Make sure the scene loads completely (map w/obstacles and Pioneer robot).
		d) In top ribbon, click the right-pointing arrow to start simulation.
		e) Once the robot reaches within the threshokd siatnce of the goal node, both motors will stop moving.
		f) Feel free to open up the "Pioneer_p3dx" non-threaded child script within the left menu / scene hierarchy.
			o Note that this I copied this script into the "robot_child_script_longerScenario.txt" file in the attached "Scenario2" folder.