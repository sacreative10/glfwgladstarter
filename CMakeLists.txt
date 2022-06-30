cmake_minimum_required(VERSION 3.0)

project(GLFWStarter)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
# only here for folks that rely on compile_commands.json
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# add all the third party libraries
add_subdirectory(thirdParty/glfw)
include_directories(thirdParty/glad/include)

add_executable(GLFWStarter thirdParty/glad/glad.c src/main.cpp)
target_link_libraries(GLFWStarter glfw3)




