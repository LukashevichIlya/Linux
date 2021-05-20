cmake_minimum_required(VERSION 3.10)
project(miniFS C)

set(CMAKE_C_STANDARD 99)

include_directories(filesystem utils network)

add_executable(miniFS main.c filesystem/filesystem.c utils/utils.c)

add_executable(serverFS filesystem/filesystem.c utils/utils.c network/server.c)

add_executable(clientFS network/client.c)
