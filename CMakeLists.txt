cmake_minimum_required(VERSION 3.18)

project("gflags-playground")

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

find_package(gflags 2.2.2 EXACT REQUIRED) # PATHS "P:\\Downloads\\cpp-libraries\\portaudio\\build\\cmake\\portaudio")

IF(gflags_FOUND)
    message(STATUS "YES")
ELSE(gflags_FOUND)
    message(STATUS "NO")
ENDIF(gflags_FOUND)

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} gflags_static)
