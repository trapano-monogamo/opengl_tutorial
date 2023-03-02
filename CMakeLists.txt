cmake_minimum_required(VERSION 3.23)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(myopengl VERSION 1.0)
file(GLOB_RECURSE SRC_FILES src/*.cpp src/**/*.cpp src/*.c )
add_executable(${PROJECT_NAME} ${SRC_FILES})
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_link_directories(${PROJECT_NAME} PUBLIC lib)
target_link_libraries(${PROJECT_NAME} PUBLIC glfw3 X11)
