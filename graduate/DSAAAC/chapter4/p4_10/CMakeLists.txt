STRING( REGEX REPLACE ".*/(.*)" "\\1" CURRENT_FOLDER ${CMAKE_CURRENT_SOURCE_DIR} )
set(TARGET_NAME ${CURRENT_FOLDER})
add_executable(${TARGET_NAME}  main.c debug.h tree.c tree.h)
target_link_libraries(${TARGET_NAME} ${CONAN_LIBS})