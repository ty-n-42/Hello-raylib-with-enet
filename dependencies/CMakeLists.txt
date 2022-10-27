include(FetchContent) # prepare to fetch external content

# Add Raylib from github
FetchContent_Declare(
        raylib
        GIT_REPOSITORY "https://github.com/raysan5/raylib.git"
        GIT_TAG 4.2.0
        ) # declare the retrieval of the raylib source from github

add_subdirectory(raylib) # include ./raylib/CMakeLists.txt

# Add Enet from github
FetchContent_Declare(
        enet
#        GIT_REPOSITORY "https://github.com/lsalzman/enet.git"
        GIT_REPOSITORY "https://github.com/ty-n-42/enet.git" # use my enet fork
        GIT_TAG 529f60e2906e44ecc7aea24534d5d91624bbe4ce # branch hash for improve_cmake_config
        ) # declare the retrieval of the enet source from github

add_subdirectory(enet) # include ./enet/CMakeLists.txt