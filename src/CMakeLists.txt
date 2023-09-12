cmake_minimum_required(VERSION 3.2)
project(coroutine_task)

set(SOURCE_FILES    
    coroutinetask/coroutine_task.cpp
)

#add_library(coroutine_task SHARED STATIC ${SOURCE_FILES})

include_directories(${COROUTINE_TASK_INSTALL_LIB_DIR}/include)

#install(TARGETS coroutine_task DESTINATION ${COROUTINE_TASK_INSTALL_LIB_DIR})

# dummy exe
set(EXE_SOURCE_FILES main.cpp)
add_executable(coroutine_workflow_runner ${EXE_SOURCE_FILES})
target_link_libraries(coroutine_workflow_runner coroutine_task)

