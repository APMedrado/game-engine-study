cmake_minimum_required(VERSION 3.10)
project(MyFirstGameEngine)

set(CMAKE_CXX_STANDARD 17)

# Add SFML
set(SFML_DIR "<path_to_your_sfml_cmake_files>")
find_package(SFML 2.5 COMPONENTS graphics window system REQUIRED)

# Include directories
include_directories(include)

# Source files
file(GLOB SOURCES "src/*.cpp")

# Add executable
add_executable(MyFirstGameEngine ${SOURCES})

# Link SFML libraries
target_link_libraries(MyFirstGameEngine sfml-graphics sfml-window sfml-system)
