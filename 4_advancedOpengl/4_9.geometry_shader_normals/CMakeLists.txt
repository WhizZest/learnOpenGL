cmake_minimum_required(VERSION 3.0.0)

set(NAME 4_9.geometry_shader_normals)#修改1：修改为对应文件名


add_compile_definitions(VERTEX_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/9.3.default.vs\")
add_compile_definitions(VERTEX_NORMAL_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/9.3.normal_visualization.vs\")
add_compile_definitions(FRAGMENT_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/9.3.default.fs\")
add_compile_definitions(FRAGMENT_NORMAL_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/9.3.normal_visualization.fs\")
add_compile_definitions(GEOMETRY_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/9.3.normal_visualization.gs\")
add_compile_definitions(STB_IMAGE_IMPLEMENTATION)

add_executable(${NAME} main.cpp ${Include_Common_Dir}/camera.h ${STD_IMAGE_HEADER} ${Include_Common_Dir}/shader_m.h)

target_link_libraries(${NAME} model)