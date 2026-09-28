cmake_minimum_required(VERSION 3.20)

project(CppHttpServer LANGUAGES CXX)

add_executable(http_server 
    src/main.cpp
)

target_compile_features(http_server PRIVATE cxx_std_20)

if(MSVC)
    target_compile_options(http_server PRIVATE /W4)
endif()