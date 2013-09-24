# Author: Steven Lamerton
# Copyright: (c) 2013 Steven Lamerton
# Licence: wxWindows licence

# Set up the exe
add_executable(webview webview.cpp)

target_link_libraries(webview wvwk ${wxWidgets_LIBRARIES} 
                                   ${WEBKITGTK_LIBRARIES})
