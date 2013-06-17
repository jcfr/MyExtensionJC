cmake_minimum_required(VERSION 2.8.9)

project(MyExtensionJC)

#-----------------------------------------------------------------------------
set(EXTENSION_HOMEPAGE "http://www.slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/MyExtensionJC")
set(EXTENSION_CATEGORY "Examples")
set(EXTENSION_CONTRIBUTORS "Jean-Christophe Fillion-Robin (Kitware)")
set(EXTENSION_DESCRIPTION "This is an example of extension bundling one CLI module")
set(EXTENSION_ICONURL "http://viewvc.slicer.org/viewvc.cgi/Slicer4/trunk/Extensions/Testing/MyExtensionJC/MyExtensionJC.png?revision=21745&view=co")
set(EXTENSION_SCREENSHOTURLS "http://wiki.slicer.org/slicerWiki/images/a/ab/Slicer-r19441-MyExtensionJC-screenshot.png http://wiki.slicer.org/slicerWiki/images/1/1e/Slicer-r19441-MyExtensionJC-screenshot-2.png")

#-----------------------------------------------------------------------------
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
add_subdirectory(MyCLI)

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
