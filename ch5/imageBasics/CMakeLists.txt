cmake_minimum_required( VERSION 3.0 )
project( imageBasics )

# 添加c++ 11标准支持
set( CMAKE_CXX_FLAGS "-std=c++11" )

# 寻找OpenCV库
# find opencv 3.0
#find_package( OpenCV 3.0 REQUIRED )
find_package( OpenCV REQUIRED )
# 添加头文件

find_package(Qt5 REQUIRED
        Core
        PrintSupport
        Gui
        Test
        Concurrent
        OpenGL
        Widgets
        )

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( imageBasics imageBasics.cpp )
# 链接OpenCV库
target_link_libraries( imageBasics ${OpenCV_LIBS} )
