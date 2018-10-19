cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Four_Subwindows_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Four_Subwindows_example)
target_compile_features(Four_Subwindows_example
                        PRIVATE
                        c_std_90)

target_sources(Four_Subwindows_example
               PRIVATE
               src/subwin.c)

target_link_libraries(Four_Subwindows_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
