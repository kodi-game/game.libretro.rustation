project(game.libretro.rustation)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(Kodi REQUIRED)
find_package(libretro-rustation REQUIRED)

set(DEPLIBS rustation)
set(RUSTATION_CUSTOM_BINARY ${RUSTATION_LIB}
                            ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} rustation)

build_addon(${PROJECT_NAME} RUSTATION DEPLIBS)
