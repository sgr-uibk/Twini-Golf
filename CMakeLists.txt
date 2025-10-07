cmake_minimum_required(VERSION 3.10)

project(twinigolf)

# Set the C++ standard 2014, optimization and warning flags
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -Wall -Wextra")

include_directories(SDL2)

file(GLOB SOURCES "src/*.cpp") # all .cpp files in src directory

add_executable(twinigolf ${SOURCES})

# Link against SDL2 libraries
find_package(SDL2 REQUIRED)
target_link_libraries(twinigolf SDL2main SDL2 SDL2_image SDL2_ttf SDL2_mixer)
