cmake_minimum_required(VERSION 3.10)
project(FFmpegOnMac)


link_directories(/usr/local/lib)
include_directories(/usr/local/include)


set(CMAKE_CXX_STANDARD 11)

add_executable(FFmpegOnMac main.cpp main_ffmpeg.cpp)

##---FFMpeg

#link_directories(/usr/local/lib)
#include_directories(/usr/local/include)
#include_directories(${PROJECT_SOURCE_DIR}/include)

#target_link_libraries(FFmpegOnMac /usr/local/lib/libavcodec.a)
#target_link_libraries(FFmpegOnMac /usr/local/lib/libavformat.a)
#target_link_libraries(FFmpegOnMac /usr/local/lib/libswscale.a)
#target_link_libraries(FFmpegOnMac /usr/local/lib/libavutil.a)


target_link_libraries(FFmpegOnMac  -lavformat)
target_link_libraries(FFmpegOnMac  -lavcodec)
target_link_libraries(FFmpegOnMac  -lavutil)
target_link_libraries(FFmpegOnMac  -lswscale)


##---libiconv
target_link_libraries(FFmpegOnMac  -liconv)

##---SDL2
target_link_libraries(FFmpegOnMac SDL2main SDL2)
