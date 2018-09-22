cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Shadowy_Leapin_Lizards_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Shadowy_Leapin_Lizards_example)
target_compile_features(Shadowy_Leapin_Lizards_example
                        PRIVATE
                        c_std_90)

target_sources(Shadowy_Leapin_Lizards_example
               PRIVATE
               src/dinoshade.c)

target_link_libraries(Shadowy_Leapin_Lizards_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
