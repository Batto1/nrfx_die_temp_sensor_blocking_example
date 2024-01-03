# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(temp_blocking_simple)

target_sources(app PRIVATE src/main.c)

# target_include_directories(app PUBLIC modules/hal/nordic/nrfx/samples/common)

# # Add common Kconfig file to project.
# list(APPEND CONF_FILE "${CMAKE_CURRENT_LIST_DIR}/common.conf")

# # Add project Kconfig file if it exists.
# set(PRJ_CONF_FILE "${CMAKE_CURRENT_SOURCE_DIR}/prj.conf")
# if(EXISTS ${PRJ_CONF_FILE})
#     list(APPEND CONF_FILE ${PRJ_CONF_FILE})
# endif()

# # Macro adding overlay file and Kconfig file for specified board in given directory.
# # If board-specific files have been found they are added to DTC_OVERLAY_FILE and CONF_FILE
# # symbols that are used in west build system.
# macro(GET_DEVICE_CONFIG_FILES BOARD BOARDS_DIR)
#     if(NOT IS_ABSOLUTE BOARDS_DIR)
#         set(_BOARDS_DIR ${CMAKE_CURRENT_LIST_DIR}/${BOARDS_DIR})
#         get_filename_component(BOARDS_DIR_ABSOLUTE "${_BOARDS_DIR}" ABSOLUTE)
#     else()
#         set(BOARDS_DIR_ABSOLUTE {BOARDS_DIR})
#     endif()

#     set(OVERLAY_FILE "${BOARDS_DIR_ABSOLUTE}/${BOARD}.overlay")
#     if(EXISTS ${OVERLAY_FILE})
#         list(APPEND DTC_OVERLAY_FILE "${OVERLAY_FILE}")
#     endif()

#     set(CONFIG_FILE "${BOARDS_DIR_ABSOLUTE}/${BOARD}.conf")
#     if(EXISTS ${CONFIG_FILE})
#         list(APPEND CONF_FILE "${CONFIG_FILE}")
#     endif()
# endmacro()
