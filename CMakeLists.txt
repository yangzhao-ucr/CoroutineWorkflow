cmake_minimum_required(VERSION 3.2)

project(CoroutineWorkflow)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})

set(COROUTINE_WORKFLOW_INSTALL_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)
set(COROUTINE_TASK_INSTALL_LIB_DIR ${PROJECT_SOURCE_DIR}/lib/coroutine_task)

# set(DIVISION_HEADERS_DIR ${PROJECT_SOURCE_DIR}/src/division)

include_directories(${COROUTINE_WORKFLOW_INSTALL_INCLUDE_DIR})
include_directories(${COROUTINE_TASK_INSTALL_LIB_DIR}/include)

add_subdirectory(lib/coroutine_task)
add_subdirectory(src)
#add_subdirectory(test)