set (lib_name cesl_containers)

add_library(${lib_name} STATIC "")

target_sources(${lib_name}
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/cesl_vector_s.h
    PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/cesl_vector_s.c
)

target_link_libraries(${lib_name} cesl_compiler)
get_filename_component(PARENT_DIR ${CMAKE_CURRENT_SOURCE_DIR} DIRECTORY)
target_include_directories(${lib_name} INTERFACE ${PARENT_DIR})

add_subdirectories_standard()
