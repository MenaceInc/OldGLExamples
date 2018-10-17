cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Two_Sided_Lighting_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Two_Sided_Lighting_example)
target_compile_features(Two_Sided_Lighting_example
                        PRIVATE
                        c_std_90)

target_sources(Two_Sided_Lighting_example
               PRIVATE
               src/olight.c)

target_link_libraries(Two_Sided_Lighting_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
