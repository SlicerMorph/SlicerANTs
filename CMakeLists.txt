cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(ANTsWasm)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/ANTsWasm")
set(EXTENSION_CATEGORY "Registration")
set(EXTENSION_CONTRIBUTORS "Dženan Zukić (Kitware Inc.)")
set(EXTENSION_DESCRIPTION "ANTs computes high-dimensional mapping to capture the statistics of brain structure and function. This is a Slicer extension for exposing ANTsWasm, a package which provides a WebAssembly, Python, and C++ interfaces to ANTs. This interface is a performant interface inspired by ANTsPy and ANTsR.")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/ANTsWasm.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/ANTsWasm/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(ITKANTsCommon)
add_subdirectory(ANTsRegistration)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
