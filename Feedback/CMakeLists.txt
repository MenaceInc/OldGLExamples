cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Feedback_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Feedback_example)
target_compile_features(Feedback_example
                        PRIVATE
                        c_std_90)

target_sources(Feedback_example
               PRIVATE
               src/trippy.c)

target_link_libraries(Feedback_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
