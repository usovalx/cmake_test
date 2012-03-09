
add_custom_command(
    OUTPUT ${CMAKE_CURRENT_SOURCE_DIR}/tt.h ${CMAKE_CURRENT_SOURCE_DIR}/tt.c
    COMMAND ${CMAKE_CURRENT_SOURCE_DIR}/gen.sh
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    VERBATIM)

add_custom_target(sub2Hxx
    DEPENDS ${CMAKE_CURRENT_SOURCE_DIR}/tt.h ${CMAKE_CURRENT_SOURCE_DIR}/tt.c)

add_library(t2
    gen.sh
    tt.c tt.h
    )
    # main.c)

add_dependencies(t2 sub2Hxx)
