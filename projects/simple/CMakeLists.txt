CMAKE_MINIMUM_REQUIRED(VERSION 3.12)

PROJECT( simple )

ADD_EXECUTABLE(${PROJECT_NAME}
	src/main.cpp
	src/header.cpp

	include/header.hpp

	../../more/TODO.txt
	CMakeLists.txt
)

TARGET_INCLUDE_DIRECTORIES( ${PROJECT_NAME} PUBLIC
	include
)











