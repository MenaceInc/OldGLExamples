cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Lighting_Laboratory_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Lighting_Laboratory_example)
target_compile_features(Lighting_Laboratory_example
                        PRIVATE
                        c_std_90)

target_sources(Lighting_Laboratory_example
               PRIVATE
               src/lightlab.c)

target_link_libraries(Lighting_Laboratory_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
