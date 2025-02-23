cmake_minimum_required(VERSION 3.5)
project(DJ LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FetchContent)
FEtchCOntent_Declare(
    cpr
    GIT_REPOSITORY https://github.com/libcpr/cpr.git
    GIT_TAG 1.11.2
)

FetchContent_MakeAvailable(cpr)

add_executable(dj main.cpp)
target_link_libraries(dj PRIVATE cpr::cpr)