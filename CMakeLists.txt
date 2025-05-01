cmake_minimum_required(VERSION 3.19)
project(engine)

add_definitions(-DSAMPLE_ROOT="${PROJECT_SOURCE_DIR}/sample")

set(CMAKE_C_STANDARD 11)

add_executable(msdf_sample sample/sample.c)
if(WIN32)
    target_compile_definitions(msdf_sample PRIVATE _CRT_SECURE_NO_WARNINGS)
endif()
target_include_directories(msdf_sample PRIVATE modules/xhl/include)