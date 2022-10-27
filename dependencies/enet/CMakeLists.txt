message(STATUS "Fetching enet. Be patient. The may take a while.")

FetchContent_MakeAvailable(enet) # fetch enet and make it available to cmake
# the enet header file (enet.h) should be available to include like this: #include "enet/enet.h"