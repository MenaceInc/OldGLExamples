cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Highlight_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Highlight_example)
target_compile_features(Highlight_example
                        PRIVATE
                        c_std_90)

target_sources(Highlight_example
               PRIVATE
               src/highlight.c)

target_link_libraries(Highlight_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
