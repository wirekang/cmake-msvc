cmake_minimum_required(VERSION 3.30.0)
set(CMAKE_CXX_STANDARD 17)



set(LOCAL_PROJECT_NAME "__project_name__")
set(LOCAL_PROJECT_VERSION "0.0.1")

set(OPTIONS
)

set(DEFINES

)

set(SOURCES
    main.cc
    sample.cc
)

project(${LOCAL_PROJECT_NAME} VERSION ${LOCAL_PROJECT_VERSION} LANGUAGES C CXX)

add_executable(${LOCAL_PROJECT_NAME})

list(TRANSFORM SOURCES PREPEND "src/")

target_sources(${LOCAL_PROJECT_NAME} PRIVATE ${SOURCES} ${HEADERS})
target_compile_definitions(${LOCAL_PROJECT_NAME} PRIVATE ${DEFINES})
target_compile_options(${LOCAL_PROJECT_NAME} PRIVATE ${OPTIONS})

set_target_properties(${LOCAL_PROJECT_NAME} PROPERTIES RUNTIME_OUTPUT_DIRECTORY "bin")





#################
# Dependencies
#################
