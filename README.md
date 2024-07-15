# Creating-2D-Occupancy-Grid-Map-using-overhead-infrastructure-cameras
Creating a 2D occupancy grid map using overhead infrastructure cameras in a ROS environment involves capturing images from the cameras, processing these images to detect obstacles, and generating the occupancy grid map. This map represents the environment in a 2D grid where each cell indicates whether it is occupied. The process includes setting up the ROS workspace, configuring the cameras, processing the image data using computer vision techniques, and publishing the occupancy grid map. The map is then used in Gazebo for simulation, enabling visualization and interaction within a simulated environment.

In the initial phase, you will need to equip a room or area with four overhead RGB cameras
arranged in a 2x2 pattern, ensuring some overlap in their fields of view. The room should contain
static objects such as chairs, tables, stools, and boxes. Using the images from these cameras, and
by stitching the views together, you will create a 2D occupancy grid map of the room. The goal is
to demonstrate that this map can be effectively used by AMRs for path-planning and navigation.

In the second phase, the room environment will become dynamic, meaning objects like tables and
chairs can be moved around. The 2D occupancy grid map should be able to dynamically update
itself to reflect these changes, providing a new, accurate map for AMRs to navigate. Additionally,
you will add semantic labels to the map (e.g., "table", "chair", "other AMR") to provide further
context for the AMRs. This will likely require the implementation of simple object detection.
