cmake_minimum_required(VERSION 3.0.0)

set(NAME 4_6Cubemaps_Reflect_Refract)#修改1：修改为对应文件名


add_compile_definitions(VERTEX_CUBE_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/6.2.cubemaps.vs\")
add_compile_definitions(VERTEX_SKYBOX_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/6.2.skybox.vs\")
add_compile_definitions(FRAGMENT_CUBE_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/6.2.cubemaps.fs\")
add_compile_definitions(FRAGMENT_REFRACT_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/refract.fs\")
add_compile_definitions(FRAGMENT_SKYBOX_FILE=\"${CMAKE_CURRENT_SOURCE_DIR}/6.2.skybox.fs\")
add_compile_definitions(STB_IMAGE_IMPLEMENTATION)

add_executable(${NAME} main.cpp ${Include_Common_Dir}/camera.h ${STD_IMAGE_HEADER} ${Include_Common_Dir}/shader_m.h)

target_link_libraries(${NAME} model)