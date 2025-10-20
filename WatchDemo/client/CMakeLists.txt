cmake_minimum_required(VERSION 4.0.0)

project(WatchDemoClient)

set(CMAKE_C_STANDARD 23)

add_executable(${PROJECT_NAME} main.c)

target_include_directories(${PROJECT_NAME} PRIVATE libs/ffmpeg/include)
target_link_directories(${PROJECT_NAME} PRIVATE libs/ffmpeg/lib)
target_link_libraries(${PROJECT_NAME} PRIVATE avcodec avformat avutil)