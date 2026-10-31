cmake_minimum_required(VERSION 4.3.3) # Set CMake version
set(CMAKE_CXX_STANDARD 23) #            Set C++ Standard
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include("./cmake/project-meta-config.cmake")

project(${PROJECT_NAME} # Project meta-information used by CMake
    DESCRIPTION ${PROJECT_DESC}
    VERSION ${PROJECT_VER}
    HOMEPAGE_URL ${PROJECT_REPO}
    LANGUAGES CXX)

# Modules directory pathname
list(PREPEND CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake) # Modules directory
add_subdirectory("source") # Source directory
