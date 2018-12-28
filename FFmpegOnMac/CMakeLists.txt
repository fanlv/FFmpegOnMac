cmake_minimum_required(VERSION 3.10)
project(FFmpegOnMac)

set(CMAKE_CXX_STANDARD 11)

add_executable(FFmpegOnMac main.cpp)


target_link_libraries(FFmpegOnMac  -lavformat)
target_link_libraries(FFmpegOnMac  -lavcodec)
target_link_libraries(FFmpegOnMac  -lavutil)
target_link_libraries(FFmpegOnMac  -lswscale)


##---libiconv
target_link_libraries(FFmpegOnMac  -liconv)

##---SDL2
target_link_libraries(FFmpegOnMac SDL2main SDL2)
