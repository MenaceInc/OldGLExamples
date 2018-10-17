cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Stencil_Enabled_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Stencil_Enabled_example)
target_compile_features(Stencil_Enabled_example
                        PRIVATE
                        c_std_90)

target_sources(Stencil_Enabled_example
               PRIVATE
               src/ohidden.c)

target_link_libraries(Stencil_Enabled_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
