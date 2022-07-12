cmake_minimum_required(VERSION 3.12)

#Get the version from git
find_package(Git QUIET REQUIRED)
execute_process(COMMAND ${GIT_EXECUTABLE} describe --tags
                WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
                OUTPUT_VARIABLE MY_VERSION
)
message("${MY_VERSION}")
project(TestOrg VERSION ${MyVersion} LANGUAGES NONE)
