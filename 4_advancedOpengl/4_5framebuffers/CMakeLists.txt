cmake_minimum_required(VERSION 3.0.0)

set(NAME 4_5framebuffers)#修改1：修改为对应文件名


add_compile_definitions(VERTEX_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/5.1.framebuffers.vs\")
add_compile_definitions(VERTEX_SCREEN_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/5.1.framebuffers_screen.vs\")
add_compile_definitions(FRAGMENT_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/5.1.framebuffers.fs\")
add_compile_definitions(FRAGMENT_SCREEN_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/5.1.framebuffers_screen.fs\")
add_compile_definitions(STB_IMAGE_IMPLEMENTATION)

add_executable(${NAME} main.cpp ${Include_Common_Dir}/camera.h ${STD_IMAGE_HEADER} ${Include_Common_Dir}/shader_m.h)

target_link_libraries(${NAME} model)