cmake_minimum_required(VERSION 3.5)

project(QCustomPlot)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)

#find_package(QT NAMES Qt6 Qt5 COMPONENTS Widgets PrintSupport REQUIRED)
find_package(Qt5 COMPONENTS Widgets PrintSupport REQUIRED)

add_library(QCustomPlot STATIC
    qcustomplot.cpp
    )

target_link_libraries(QCustomPlot PUBLIC Qt5::Widgets Qt5::PrintSupport)
