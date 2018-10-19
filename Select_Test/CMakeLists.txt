cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Select_Test_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Select_Test_example)
target_compile_features(Select_Test_example
                        PRIVATE
                        c_std_90)

target_sources(Select_Test_example
               PRIVATE
               src/triselect.c)

target_link_libraries(Select_Test_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
