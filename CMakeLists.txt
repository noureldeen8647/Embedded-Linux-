cmake_minimum_required(VERSION 3.16.3)
project(CarEngine)

set(CMAKE_CXX_STANDARD 17)

# Add the path to the gtest source code directory
add_subdirectory(gtest)

# Add your own source files
add_executable(Test main.cpp car_test.cpp car.cpp)

# Link against gtest library
target_link_libraries(Test PRIVATE gmock_main)
