cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Red_3D_Lighted_Cube_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Red_3D_Lighted_Cube_example)
target_compile_features(Red_3D_Lighted_Cube_example
                        PRIVATE
                        c_std_90)

target_sources(Red_3D_Lighted_Cube_example
               PRIVATE
               src/cube.c)

target_link_libraries(Red_3D_Lighted_Cube_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
