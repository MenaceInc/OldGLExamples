cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(MJK_Warp_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(MJK_Warp_example)
target_compile_features(MJK_Warp_example
                        PRIVATE
                        c_std_90)

target_sources(MJK_Warp_example
               PRIVATE
               src/mjkimage.c
               src/mjkwarp.c)

target_link_libraries(MJK_Warp_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
