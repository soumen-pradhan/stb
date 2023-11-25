cmake_minimum_required(VERSION 3.24)
project(stb C)

add_library(${PROJECT_NAME} INTERFACE)
add_library(${PROJECT_NAME}::${PROJECT_NAME} ALIAS ${PROJECT_NAME})

set_target_properties(${PROJECT_NAME}
    PROPERTIES
        C_STANDARD 90
        C_STANDARD_REQUIRED ON
        C_EXTENSIONS OFF
)

target_sources(${PROJECT_NAME}
    INTERFACE
        FILE_SET HEADERS
        FILES
            stb_image.h
            stb_image_write.h
)
