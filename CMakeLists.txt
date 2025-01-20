cmake_minimum_required(VERSION 3.31.3 FATAL_ERROR)
project(metal-cpp VERSION 1.0.0)

add_library(metal-cpp)
target_include_directories(metal-cpp PUBLIC "include")
target_sources(metal-cpp PRIVATE "src/metal.cpp")
target_compile_features(metal-cpp PRIVATE cxx_std_17)
target_link_libraries(metal-cpp PRIVATE "-framework Metal" "-framework Foundation" "-framework Cocoa" "-framework CoreGraphics" "-framework MetalKit")