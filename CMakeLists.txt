cmake_minimum_required(VERSION 3.0.2)
project(tetra_calibrator)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)

catkin_package()

install(DIRECTORY /
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(PROGRAMS
  ${CATKIN_DEVEL_PREFIX}/lib/calibrator/chessboard
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
