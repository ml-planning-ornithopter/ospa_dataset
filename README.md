# ospa_dataset

This project contains three dataset files of trajectory optimization for ornithopters. Each file is composed with a large number of optimal flight trajetories for an ornithopter in the 2D space. Trajectories consist in a set of consecutive flight states connecting an initial and a target states. The optimal trajectories are computed using the ornithopter prototype and the optimization algorithm provided in https://arxiv.org/abs/2010.12273

The planning problem is divided in two phases, the mid-range problem and the landing problem. The first is the problem of planning the optimal flight trajectory for medium distances: X in [25, 100] meters and Z in [-40, 0] meters. In the other hand, the landing problem is a short-distance planning: X in [15, 25] meters and Z in [-10, 0] meters. The landing is an important maneuver that requires high precision because is the preceding step to the perching of the ornithopter.     

Each dataset contains the following columns:

1. id_trajectory: Trajectory identifier
2. id_in_seq: Numbers of consecutive states in the trajectory
3. initial state: Initial State 	
4. current_state:	Sequence of consecutive states in the trajectory
5- goal_state: Target state 
6- out_action: Sequence of consecutive constrol maneuvers during the flight trajectory (rad, Hz)	
7- timesteps: Time step between consecutive control maneuvers (s)

Flight states consist in a set of variables:

1- X axis position (m)
2- Z axis position (m)
3- Velocity in the X axis (m/s)
4- Velocity in the Z axis (m/s)
5- Pitch value (rad)
6- Angular velocity (rad/s)

DATASETS:
* OSPA_medium-range_training_data.csv  : The training dataset for the mid-range planning
* OSPA_landing_training_data.csv       : The training dataset for the landing problem
* OSPA_landing_validation_data.csv     : The validation dataset for the landing problem

As far as we know there is no data available for ornithopter trajectory optimization.


