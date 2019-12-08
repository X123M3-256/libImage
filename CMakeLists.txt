cmake_minimum_required (VERSION 3.1)
project (Image C)

add_library(Image STATIC src/image.c)
set_property(TARGET Image PROPERTY C_STANDARD 99)

