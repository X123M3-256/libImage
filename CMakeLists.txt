cmake_minimum_required (VERSION 3.1)
project (Image C)

add_library(Image STATIC src/image.c)

find_package(PNG REQUIRED)
include_directories(${PNG_INCLUDE_DIR})
target_link_libraries(Image ${PNG_LIBRARY})

set_property(TARGET Image PROPERTY C_STANDARD 99)

add_executable(TestImage src/main.c)
set_property(TARGET TestImage PROPERTY C_STANDARD 99)
target_link_libraries (TestImage Image)
