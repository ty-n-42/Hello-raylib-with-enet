message(STATUS "Fetching raylib. Be patient, this may take a while.")

set(BUILD_EXAMPLES OFF CACHE BOOL "" FORCE) # don't build the supplied examples
set(BUILD_GAMES    OFF CACHE BOOL "" FORCE) # don't build the supplied example games

FetchContent_MakeAvailable(raylib) # fetch raylib and make it available to cmake
# raylib should be downloaded and built in the build folder
# the raylib header files (raylib.h, raymath.h, rlgl.h) should be available to include like this: #include "raylib.h"