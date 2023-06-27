cmake_minimum_required(VERSION 3.19)
cmake_policy(VERSION 3.19)

# Initialize Mbed OS build system. 
# Note: This block must be before the include of app.cmake
set(MBED_APP_JSON_PATH mbed_app.json)

include(mbed-os/tools/cmake/app.cmake)
add_subdirectory(mbed-os)

project(RemoteIR-Test-Program)

add_subdirectory(RemoteIR)

# TextLCD has not been converted to an Mbed CE library yet so we have to build it in CMake here
add_library(TextLCD TextLCD/TextLCD.cpp)
target_include_directories(TextLCD PUBLIC TextLCD)
target_link_libraries(TextLCD PUBLIC mbed-core-flags)

add_executable(RemoteIR-Test-Program main.cpp)
target_link_libraries(RemoteIR-Test-Program RemoteIR TextLCD mbed-os) # Can also link to mbed-baremetal here
mbed_set_post_build(RemoteIR-Test-Program)

mbed_finalize_build()