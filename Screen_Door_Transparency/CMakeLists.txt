cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Screen_Door_Transparency_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Screen_Door_Transparency_example)
target_compile_features(Screen_Door_Transparency_example
                        PRIVATE
                        c_std_90)

target_sources(Screen_Door_Transparency_example
               PRIVATE
               src/screendoor.c)

target_link_libraries(Screen_Door_Transparency_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
