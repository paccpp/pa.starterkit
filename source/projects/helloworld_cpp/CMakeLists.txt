cmake_minimum_required(VERSION 3.0)

set(PRODUCT_NAME ${project_dir})
set(PROJECT_NAME ${project_dir})

file(GLOB_RECURSE PROJECT_INCLUDES
	${CMAKE_CURRENT_SOURCE_DIR}/*.h
	${CMAKE_CURRENT_SOURCE_DIR}/*.hpp
)

file(GLOB_RECURSE PROJECT_SRC
	${CMAKE_CURRENT_SOURCE_DIR}/*.c
	${CMAKE_CURRENT_SOURCE_DIR}/*.cpp
	${PROJECT_INCLUDES}
)

set(PROJECT_FILES
	${PROJECT_SRC}
	${PROJECT_INCLUDES}
)

add_executable(${PRODUCT_NAME} "${PROJECT_FILES}")
