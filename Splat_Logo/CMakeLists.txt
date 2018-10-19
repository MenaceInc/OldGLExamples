cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Splat_Logo_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Splat_Logo_example)
target_compile_features(Splat_Logo_example
                        PRIVATE
                        c_std_90)

target_sources(Splat_Logo_example
               PRIVATE
               src/splatlogo.c
               src/logo.c)

target_link_libraries(Splat_Logo_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
