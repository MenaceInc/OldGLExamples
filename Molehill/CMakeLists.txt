cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Molehill_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Molehill_example)
target_compile_features(Molehill_example
                        PRIVATE
                        c_std_90)

target_sources(Molehill_example
               PRIVATE
               src/molehill.c)

target_link_libraries(Molehill_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
