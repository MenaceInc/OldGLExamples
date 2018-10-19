cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Texture_Environment_Test_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Texture_Environment_Test_example)
target_compile_features(Texture_Environment_Test_example
                        PRIVATE
                        c_std_90)

target_sources(Texture_Environment_Test_example
               PRIVATE
               src/texenv.c)

target_link_libraries(Texture_Environment_Test_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
