
CMAKE_MINIMUM_REQUIRED(VERSION 3.1...3.15)

if(${CMAKE_VERSION} VERSION_LESS 3.12)
	CMAKE_POLICY(VERSION ${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION})
ENDIF()

MESSAGE(STATUS "CMake version: " ${CMAKE_MAJOR_VERSION} "." ${CMAKE_MINOR_VERSION})

PROJECT(project_name
	VERSION 1.0
	DESCRIPTION "This is for CMake testing"
	LANGUAGES CXX)

set(target_name ${PROJECT_NAME})

ADD_EXECUTABLE(${target_name}	 # Name of the executable and the target
	src/main.cpp
	src/header.cpp
	# headers are ignored. We list them to show them up in the IDE
	headers/header.hpp
)

#ADD_LIBRARY(${target_name}  STATIC  # STATIC SHARED MODULE 
#	src/main.cpp
#	src/header.cpp
#	headers/header.hpp)

TARGET_INCLUDE_DIRECTORIES(${target_name} PUBLIC	# PUBLIC PRIVATE INTERFACE
	headers
)

TARGET_LINK_LIBRARIES(${target_name} PUBLIC
	#target_B
	#abc.lib
)
