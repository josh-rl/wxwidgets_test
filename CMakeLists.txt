cmake_minimum_required(VERSION 3.20)

project(wx_test VERSION 1.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_CXX_FLAGS "-Wall -Werror")

find_package(wxWidgets REQUIRED COMPONENTS core base)
include(${wxWidgets_USE_FILE})
add_subdirectory(${PROJECT_SOURCE_DIR}/src)
target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})
