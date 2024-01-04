cmake_minimum_required(VERSION 3.10)

project(bmp2text)

#set_property(TARGET zbar_app PROPERTY C_STANDARD 99)
set(CMAKE_C_FLAGS "-std=c99")

# for Cortex-A series
#SET(CMAKE_C_COMPILER   arm-none-linux-gnueabihf-gcc)
#SET(CMAKE_CXX_COMPILER arm-none-linux-gnueabihf-g++)

# for ARM9 series

#SET(CMAKE_C_COMPILER   arm-buildroot-linux-gnueabi-gcc)
#SET(CMAKE_CXX_COMPILER arm-buildroot-linux-gnueabi-g++)

# for Ubuntu
SET(CMAKE_C_COMPILER   gcc)
SET(CMAKE_CXX_COMPILER g++)

aux_source_directory(. DIR_SRCS)

add_executable(bmp2text ${DIR_SRCS})

