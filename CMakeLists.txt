cmake_minimum_required(VERSION 2.8.3)
project(reem_rgbd_launch)

find_package(catkin REQUIRED COMPONENTS
  dynamic_reconfigure
  openni2_launch
  rospy
)

catkin_package()

install(PROGRAMS scripts/set_xtion_dyn_params.py scripts/__init__.py scripts/set_simulated_xtion_dyn_params.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch)
  
install(DIRECTORY config/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/config)
