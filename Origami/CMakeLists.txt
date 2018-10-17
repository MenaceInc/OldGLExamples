cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Origami_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Origami_example)
target_compile_features(Origami_example
                        PRIVATE
                        c_std_90)

target_sources(Origami_example
               PRIVATE
               src/origami.c)

target_link_libraries(Origami_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
