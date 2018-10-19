cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Surface_Grid_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Surface_Grid_example)
target_compile_features(Surface_Grid_example
                        PRIVATE
                        c_std_90)

target_sources(Surface_Grid_example
               PRIVATE
               src/surfgrid.c)

target_link_libraries(Surface_Grid_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
