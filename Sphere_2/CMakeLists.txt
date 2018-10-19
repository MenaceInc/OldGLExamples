cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Sphere_2_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Sphere_2_example)
target_compile_features(Sphere_2_example
                        PRIVATE
                        c_std_90)

target_sources(Sphere_2_example
               PRIVATE
               src/sphere2.c)

target_link_libraries(Sphere_2_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
