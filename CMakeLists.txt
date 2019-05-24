cmake_minimum_required(VERSION 3.7.2)
project(hello)

# Build a release version
#set(CMAKE_BUILD_TYPE Release)

include_directories(include)

# include all cpp...
file(GLOB SOURCES "src/*.cpp")

# ... or specify by file
#set(SOURCES src/hello_world.cpp)

# Include a shared/static library
#set(PROJECT_LINK_LIBS libMyLibrary.so libMyLibrary2.a)
#link_directories(/usr/lib)
 
# Create executable
add_executable(hello ${SOURCES})

# Create a shared library; types are SHARED, STATIC or MODULE
# add_library(hello_shared SHARED ${SOURCES})

# Set the location for -- i.e., /usr/lib or /usr/bin
# Use "sudo make install" to apply
# install(TARGETS hello DESTINATION /usr/bin)


# Useful commands:
# ldd libhello_shared.so		shows dependencies
# ar -t libhello_static.a		shows content of library
# nm -C libhello_static.a		shows symbols

