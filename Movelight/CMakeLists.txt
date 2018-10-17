cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Movelight_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Movelight_example)
target_compile_features(Movelight_example
                        PRIVATE
                        c_std_90)

target_sources(Movelight_example
               PRIVATE
               src/Movelight.c)

target_link_libraries(Movelight_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
