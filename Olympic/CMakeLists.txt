cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Olympic_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Olympic_example)
target_compile_features(Olympic_example
                        PRIVATE
                        c_std_90)

target_sources(Olympic_example
               PRIVATE
               src/olympic.c)

target_link_libraries(Olympic_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
