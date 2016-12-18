cmake_minimum_required(VERSION 2.6)
project(LinuxSerialPort)

include_directories(inc)
SET(CMAKE_CXX_FLAGS "-std=c++0x") #启用C++11
add_subdirectory(src)

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} SerialPort pthread)

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION bin)
