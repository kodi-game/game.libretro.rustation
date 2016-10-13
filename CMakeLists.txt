cmake_minimum_required(VERSION 3.1)
project(game.libretro.rustation)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-rustation REQUIRED)

set(DEPLIBS rustation)
set(RUSTATION_CUSTOM_BINARY ${RUSTATION_LIB}
                            ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} RUSTATION DEPLIBS)
