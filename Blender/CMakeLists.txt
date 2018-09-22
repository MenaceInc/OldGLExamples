cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Blender_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Blender_example)
target_compile_features(Blender_example
                        PRIVATE
                        c_std_90)

target_sources(Blender_example
               PRIVATE
               src/blender.c)

target_link_libraries(Blender_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
