cmake_minimum_required(VERSION 3.10)
project(DSA_CPP)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Enable more warnings for professional level code
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -pedantic")

# Find all C++ source files
file(GLOB_RECURSE SOURCES "*.cpp")

foreach(source_file IN LISTS SOURCES)
    # Get the file name without extension
    get_filename_component(target_name ${source_file} NAME_WE)
    
    # Optional: handle duplicate names by prefixing directory name if needed
    # get_filename_component(dir_name ${source_file} DIRECTORY)
    # get_filename_component(dir_name ${dir_name} NAME)
    # set(target_name "${dir_name}_${target_name}")
    
    # Avoid creating targets for files we want to skip, if any
    # (assuming all standalone .cpp files in this repo have a main function)
    if(NOT ${target_name} STREQUAL "tempCodeRunnerFile")
        # Check if target already exists (in case of duplicate filenames in different folders)
        if(TARGET ${target_name})
            set(target_name "${target_name}_dup")
        endif()
        
        add_executable(${target_name} ${source_file})
    endif()
endforeach()
