cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Dinoball_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Dinoball_example)
target_compile_features(Dinoball_example
                        PRIVATE
                        c_std_90)

target_sources(Dinoball_example
               PRIVATE
               src/dinoball.c)

target_link_libraries(Dinoball_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
