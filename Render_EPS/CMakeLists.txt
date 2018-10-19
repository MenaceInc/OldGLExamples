cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Render_EPS_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Render_EPS_example)
target_compile_features(Render_EPS_example
                        PRIVATE
                        c_std_90)

target_sources(Render_EPS_example
               PRIVATE
               src/rendereps.c)

target_link_libraries(Render_EPS_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
