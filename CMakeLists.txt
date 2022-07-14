cmake_minimum_required(VERSION 3.0)

project(GLFWStarter)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
# only here for folks that rely on compile_commands.json
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_CXX_FLAGS_DEBUG_INIT "-Wall -g")
set(CMAKE_CXX_FLAGS_RELEASE_INIT "-O3")

# add all the third party libraries
add_subdirectory(thirdParty/glfw)
include_directories(thirdParty/glad/include)

add_executable(GLFWStarter thirdParty/glad/glad.c src/main.cpp src/util/logger.cpp src/util/GLutil.cpp)
target_link_libraries(GLFWStarter glfw3)




