cmake_minimum_required(VERSION 3.1)
project(game.libretro.bnes)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-bnes REQUIRED)

set(BNES_CUSTOM_BINARY ${BNES_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BNES "")

include(CPack)
