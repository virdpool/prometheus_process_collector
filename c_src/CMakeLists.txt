# RandomX works? So copypaste stuff from there

cmake_minimum_required(VERSION 2.8.7)

project(prometheus_process_collector)

set(prometheus_process_collector_sources
prometheus_process_info_windows.cc
prometheus_process_collector_nif.cc)


include_directories("c:/Program Files/erl-24.3.4.6/usr/include")
# include_directories("c:/Program Files/erl-24.3.4.6/usr/lib")
# credits https://github.com/georgegerdin/nuklear-examples-vcpkg/blob/master/unistd.h
include_directories("win")
# 
add_executable(prometheus_process_collector ${prometheus_process_collector_sources})
# set_property(TARGET prometheus_process_collector PROPERTY C_STANDARD 99)
# target_link_libraries(prometheus_process_collector PUBLIC "c:/Program Files/erl-24.3.4.6/usr/lib/ei.lib")
# target_link_libraries(prometheus_process_collector PUBLIC "c:/Program Files/erl-24.3.4.6/usr/lib/ei_md.lib")
# 
# set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /NODEFAULTLIB:LIBCMT")
# 
# # fix ei.h
# add_definitions(-D__WIN32__)
