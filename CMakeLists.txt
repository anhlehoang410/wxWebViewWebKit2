# Author: Steven Lamerton
# Copyright: (c) 2013 Steven Lamerton
# Licence: wxWindows licence

# Required to find the webview library
cmake_minimum_required(VERSION 2.8.8)

project(wxwebviewwebkit2)

# Find WebKitGTK+
include(FindPkgConfig)
pkg_check_modules(WEBKITGTK webkit2gtk-3.0>=2.0.0)
include_directories(${WEBKITGTK_INCLUDE_DIRS})

# Set up the source and header files
set(source webview_webkit2.cpp)
set(headers webview_webkit2.h)

# Find wxWidgets
find_package(wxWidgets COMPONENTS webview adv xml stc core base REQUIRED)
include(${wxWidgets_USE_FILE})

# Add wxwebviewwebkit2 to a simple library so we can use it in all samples
add_library(wvwk STATIC ${source} ${headers})

add_subdirectory(samples)
