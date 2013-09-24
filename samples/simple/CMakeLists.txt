# Author: Steven Lamerton
# Copyright: (c) 2013 Steven Lamerton
# Licence: wxWindows licence

# Set up the exe
add_executable(simple simple.cpp simple.h)

target_link_libraries(simple wvwk ${wxWidgets_LIBRARIES} 
                                  ${WEBKITGTK_LIBRARIES})

