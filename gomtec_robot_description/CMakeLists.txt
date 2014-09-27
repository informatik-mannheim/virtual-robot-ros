cmake_minimum_required(VERSION 2.8.3)

project(gomtec_robot_description)

find_package(catkin REQUIRED)

catkin_package()

foreach(dir doc launch meshes urdf)
  install(
    DIRECTORY ${dir}/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach()

install(FILES urdf.rviz DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
