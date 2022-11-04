# RandomX works? So copypaste stuff from there

cmake_minimum_required(VERSION 2.8.7)

project(prometheus_process_collector)

set(prometheus_process_collector_sources
prometheus_process_info_windows.cc
prometheus_process_collector_nif.cc)


include_directories("c:/Program Files/erl-24.3.4.6/usr/include")

# credits https://github.com/georgegerdin/nuklear-examples-vcpkg/blob/master/unistd.h
include_directories("win")

add_library(prometheus_process_collector SHARED ${prometheus_process_collector_sources})
