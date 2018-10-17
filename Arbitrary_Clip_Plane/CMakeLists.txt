cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Arbitrary_Clip_Plane_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Arbitrary_Clip_Plane_example)
target_compile_features(Arbitrary_Clip_Plane_example
                        PRIVATE
                        c_std_90)

target_sources(Arbitrary_Clip_Plane_example
               PRIVATE
               src/oclip.c)

target_link_libraries(Arbitrary_Clip_Plane_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
