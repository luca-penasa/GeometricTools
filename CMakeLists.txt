project(GeometricTools)
cmake_minimum_required(VERSION 2.8)

if(${CMAKE_SYSTEM_NAME} MATCHES "Linux")
	message("\nLinux OS detected: ${CMAKE_SYSTEM}")
	set(__LINUX__ TRUE)
elseif(${CMAKE_SYSTEM_NAME} MATCHES "Darwin")
	message("\nMac OS X detected: ${CMAKE_SYSTEM}")
	set(__MAC_OS_X__ TRUE)
endif()

add_definitions(-DGTE_NO_LOGGER)


# Static by default.
#set (BUILD_SHARED_LIBS OFF)
add_definitions(-DUNICODE)

include_directories (GTEngine/Include)
add_subdirectory (GTEngine/Source)

#install (DIRECTORY GTEngine/Include/ DESTINATION include FILES_MATCHING PATTERN "*.h")
