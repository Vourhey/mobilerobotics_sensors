cmake_minimum_required(VERSION 2.8.3)
project(rpi_sensors)

find_package(catkin REQUIRED
    COMPONENTS
        rospy
        robonomics_lighthouse
)

catkin_python_setup()

catkin_package()

catkin_install_python(
    PROGRAMS
        scripts/get_sensors_data
    DESTINATION
        ${CATKIN_PACKAGE_BIN_DESTINATION}
)
