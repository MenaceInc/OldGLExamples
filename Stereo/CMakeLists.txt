cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Stereo_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Stereo_example)
target_compile_features(Stereo_example
                        PRIVATE
                        c_std_90)

target_sources(Stereo_example
               PRIVATE
               src/stereo.c)

target_link_libraries(Stereo_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
