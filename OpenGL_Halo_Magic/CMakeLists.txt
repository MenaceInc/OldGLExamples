cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(OpenGL_Halo_Magic_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(OpenGL_Halo_Magic_example)
target_compile_features(OpenGL_Halo_Magic_example
                        PRIVATE
                        c_std_90)

target_sources(OpenGL_Halo_Magic_example
               PRIVATE
               src/halomagic.c)

target_link_libraries(OpenGL_Halo_Magic_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
