
add_custom_command(
    OUTPUT tt.h tt.c
    COMMAND ${CMAKE_CURRENT_SOURCE_DIR}/gen.sh
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    VERBATIM)

add_executable(t2
    gen.sh
    tt.c tt.h
    main.c)