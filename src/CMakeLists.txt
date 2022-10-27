add_executable(a_out) # declare an executable be built: a_out.exe
# executable is created: <build folder>/src/a_out.exe
# the build folder is automagically created by cmake in the directory where the projects CMakeLists.txt is

target_sources(a_out PRIVATE main.c) # defines the build dependencies for a_out
# populates the SOURCES property of a_out with main.c

target_link_libraries(a_out PRIVATE raylib enet) # define the build library dependencies for a_out
# PRIVATE causes raylib and enet to only be linked to a_out


# --==== FROM SOME OTHER EXAMPLE ====--
# Adding our source files
#file(GLOB_RECURSE PROJECT_SOURCES CONFIGURE_DEPENDS "${CMAKE_CURRENT_LIST_DIR}/sources/*.c") # Define PROJECT_SOURCES as a list of all source files
#set(PROJECT_INCLUDE "${CMAKE_CURRENT_LIST_DIR}/sources/") # Define PROJECT_INCLUDE to be the path to the include directory of the project

# Declaring our executable
#add_executable(${PROJECT_NAME})
#target_sources(${PROJECT_NAME} PRIVATE ${PROJECT_SOURCES})
#target_include_directories(${PROJECT_NAME} PRIVATE ${PROJECT_INCLUDE})
#target_link_libraries(${PROJECT_NAME} PRIVATE raylib enet)

# Setting ASSETS_PATH
#target_compile_definitions(${PROJECT_NAME} PUBLIC ASSETS_PATH="${CMAKE_CURRENT_SOURCE_DIR}/assets/") # Set the asset path macro to the absolute path on the dev machine
#target_compile_definitions(${PROJECT_NAME} PUBLIC ASSETS_PATH="./assets") # Set the asset path macro in release mode to a relative path that assumes the assets folder is in the same directory as the game executable
