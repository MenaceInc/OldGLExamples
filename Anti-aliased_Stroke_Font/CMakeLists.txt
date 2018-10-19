cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Anti-aliased_Stroke_Font_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Anti-aliased_Stroke_Font_example)
target_compile_features(Anti-aliased_Stroke_Font_example
                        PRIVATE
                        c_std_90)

target_sources(Anti-aliased_Stroke_Font_example
               PRIVATE
               src/stroke.c)

target_link_libraries(Anti-aliased_Stroke_Font_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
