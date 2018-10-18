cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Scene_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Scene_example)
target_compile_features(Scene_example
                        PRIVATE
                        c_std_90)

target_sources(Scene_example
               PRIVATE
               src/scene.c)

target_link_libraries(Scene_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
