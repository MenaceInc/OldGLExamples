cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Dinospin_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Dinospin_example)
target_compile_features(Dinospin_example
                        PRIVATE
                        c_std_90)

target_sources(Dinospin_example
               PRIVATE
               src/dinospin.c
               src/trackball.c)

target_link_libraries(Dinospin_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
