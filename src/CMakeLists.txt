add_executable(3dcalculator "main.cpp"
"3rdparty/glad.c"
"3rdparty/include/imgui/imgui.cpp"
"3rdparty/include/imgui/imgui_draw.cpp"
"3rdparty/include/imgui/imgui_impl_glfw.cpp"
"3rdparty/include/imgui/imgui_impl_opengl3.cpp"
"3rdparty/include/imgui/imgui_stdlib.cpp"
"3rdparty/include/imgui/imgui_tables.cpp"
"3rdparty/include/imgui/imgui_widgets.cpp"
"orbital_camera.cpp"
"renderer.cpp"
)

set_property(TARGET 3dcalculator PROPERTY CXX_STANDARD 20)

target_link_directories(3dcalculator PRIVATE "3rdparty/lib")
target_include_directories(3dcalculator PRIVATE "3rdparty/include" ".")
target_link_libraries(3dcalculator PRIVATE "glfw3" "nfd")

file(COPY "fonts" DESTINATION ".")

#target_compile_definitions(3dcalculator PRIVATE )
add_subdirectory("3rdparty")
#add_subdirectory("assets")
