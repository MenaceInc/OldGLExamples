cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(GLUT_Dials_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(GLUT_Dials_example)
target_compile_features(GLUT_Dials_example
                        PRIVATE
                        c_std_90)

target_sources(GLUT_Dials_example
               PRIVATE
               src/dials.c)

target_link_libraries(GLUT_Dials_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
