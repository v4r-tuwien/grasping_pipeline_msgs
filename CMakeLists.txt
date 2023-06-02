cmake_minimum_required(VERSION 3.0.2)
project(grasping_pipeline_msgs)

find_package(catkin REQUIRED
    genmsg 
    actionlib
    actionlib_msgs
    std_msgs
    geometry_msgs
    vision_msgs
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  BoundingBox3DStamped.msg
)

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

# Generate actions in the 'action' folder
add_action_files(
  FILES
  FindGrasppoint.action
)

# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs 
  actionlib_msgs
  geometry_msgs
  vision_msgs
)

catkin_package()

include_directories()