cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Leapin_Lizards_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Leapin_Lizards_example)
target_compile_features(Leapin_Lizards_example
                        PRIVATE
                        c_std_90)

target_sources(Leapin_Lizards_example
               PRIVATE
               src/reflectdino.c)

target_link_libraries(Leapin_Lizards_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
