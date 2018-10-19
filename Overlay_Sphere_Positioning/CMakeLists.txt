cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Overlay_Sphere_Positioning_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Overlay_Sphere_Positioning_example)
target_compile_features(Overlay_Sphere_Positioning_example
                        PRIVATE
                        c_std_90)

target_sources(Overlay_Sphere_Positioning_example
               PRIVATE
               src/oversphere.c)

target_link_libraries(Overlay_Sphere_Positioning_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
