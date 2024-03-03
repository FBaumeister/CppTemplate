cmake_minimum_required(VERSION 3.22)


#######################################################################################################################
# Cpp Standard
#######################################################################################################################
if (NOT DEFINED CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 23)
endif()
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
#######################################################################################################################


project(SampleProject
        VERSION 1.0.0
        DESCRIPTION ""
        HOMEPAGE_URL ""
        LANGUAGES CXX C
        )

# Warning Level
include(cmake/CompilerWarnings.cmake)
EnableGlobalWarningsAsErrors()


# Subdirectories as needed...

# Proceed to submodules
add_subdirectory(libs)

# Global Examples
add_subdirectory(examples)

# Global Tests
add_subdirectory(tests)
