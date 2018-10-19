cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Zoom_Dino_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Zoom_Dino_example)
target_compile_features(Zoom_Dino_example
                        PRIVATE
                        c_std_90)

target_sources(Zoom_Dino_example
               PRIVATE
               src/zoomdino.c)

target_link_libraries(Zoom_Dino_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
