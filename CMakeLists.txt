cmake_minimum_required(VERSION 3.25)
project(matplotlib_test)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(PYTHONHOME /home/xxx/xxx/Anaconda3/envs/YOUR_PYTHON_ENV)
set(PYTHON_INCLUDE_DIR ${PYTHONHOME}/include/python3.8)
set(NUMPY_INCLUDE_DIR ${PYTHONHOME}/lib/python3.8/site-packages/numpy/core/include)
set(PYTHON_LIB ${PYTHONHOME}/lib/libpython3.8.so)
include_directories(${PYTHON_INCLUDE_DIR} ${NUMPY_INCLUDE_DIR})

add_executable(${PROJECT_NAME} main.cpp matplotlibcpp.h)
target_link_libraries(${PROJECT_NAME} ${PYTHON_LIB})


##
##
#find_package(PythonLibs 2.7)
#include_directories(/usr/local/lib/python2.7/dist-packages/numpy/core/include)
#
#
#add_definitions(-DMATPLOTLIBCPP_PYTHON_HEADER=Python.h)
#
#
#add_executable(matplotlib_test main.cpp matplotlibcpp.h)
#
#target_include_directories(matplotlib_test PRIVATE ${PYTHON_INCLUDE_DIRS})
#target_link_libraries(matplotlib_test ${PYTHON_LIBRARIES})
