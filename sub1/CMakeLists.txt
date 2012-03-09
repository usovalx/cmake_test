add_executable(t1
    main.c)
#target_link_libraries(t1 t2)

add_dependencies(t1 sub2Hxx)
