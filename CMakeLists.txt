
#include_directories(${CMAKE_CURRENT_SOURCE_DIR})
#
#nuttx_add_kernel_library(apps)
#
#include_directories(include)
#
#include(cmake/nuttx_add_application.cmake)
#
##nuttx_add_user_library(apps)
#
##add_subdirectory(canutils)
##add_subdirectory(examples)
##add_subdirectory(fsutils)
##add_subdirectory(gpsutils)
##add_subdirectory(graphics)
##add_subdirectory(import)
##add_subdirectory(interpreters)
##add_subdirectory(modbus)
##add_subdirectory(netutils)
#add_subdirectory(nshlib)
##add_subdirectory(platform)
#add_subdirectory(system)
##add_subdirectory(testing)
##add_subdirectory(tools)
##add_subdirectory(wireless)
#
#target_include_directories(apps INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})

#include(cmake/nuttx_add_application.cmake)

if (CONFIG_APPS_DIR)
  nuttx_add_library(apps)
endif()

include_directories(include)

#add_subdirectory(canutils)
#add_subdirectory(examples)
add_subdirectory(fsutils)
#add_subdirectory(gpsutils)
#add_subdirectory(graphics)
#add_subdirectory(import)
#add_subdirectory(interpreters)
#add_subdirectory(modbus)
add_subdirectory(netutils)
add_subdirectory(nshlib)
#add_subdirectory(platform)
add_subdirectory(system)
#add_subdirectory(testing)
#add_subdirectory(tools)
#add_subdirectory(wireless)

add_subdirectory(builtin) # must be last

nuttx_generate_kconfig()
