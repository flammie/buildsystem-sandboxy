# Run cmake to create some makefiles?
cmake_minimum_required(VERSION 3.10)
project(helloc VERSION 0.0.0)
add_executable(helloc hello.c)
configure_file(config.h.in config.h)

