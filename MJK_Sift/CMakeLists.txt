cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(MJK_Sift_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(MJK_Sift_example)
target_compile_features(MJK_Sift_example
                        PRIVATE
                        c_std_90)

target_sources(MJK_Sift_example
               PRIVATE
               src/mjkimage.c
               src/mjksift.c)

target_link_libraries(MJK_Sift_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
