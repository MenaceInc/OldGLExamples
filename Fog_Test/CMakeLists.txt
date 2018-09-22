cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Fog_Test_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Fog_Test_example)
target_compile_features(Fog_Test_example
                        PRIVATE
                        c_std_90)

target_sources(Fog_Test_example
               PRIVATE
               src/fogtst.c)

target_link_libraries(Fog_Test_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
