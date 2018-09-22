cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(GLUT_Plane_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(GLUT_Plane_example)
target_compile_features(GLUT_Plane_example
                        PRIVATE
                        c_std_90)

target_sources(GLUT_Plane_example
               PRIVATE
               src/glutplane.c)

target_link_libraries(GLUT_Plane_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
