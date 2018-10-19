cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Shadow_Cube_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Shadow_Cube_example)
target_compile_features(Shadow_Cube_example
                        PRIVATE
                        c_std_90)

target_sources(Shadow_Cube_example
               PRIVATE
               src/scube.c)

target_link_libraries(Shadow_Cube_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
