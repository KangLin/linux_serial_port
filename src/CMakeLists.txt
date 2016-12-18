project(SerialPort)

SET(CMAKE_CXX_FLAGS "-std=c++0x") #启用C++11

include_directories(../inc)

set(SERIAL_PORT_SOURCES serial_port.cpp poll_controler.cpp)

add_library(${PROJECT_NAME} ${SERIAL_PORT_SOURCES})
#install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION lib)