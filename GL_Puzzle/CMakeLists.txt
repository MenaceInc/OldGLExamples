cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(GL_Puzzle_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(GL_Puzzle_example)
target_compile_features(GL_Puzzle_example
                        PRIVATE
                        c_std_90)

target_sources(GL_Puzzle_example
               PRIVATE
               src/glpuzzle.c
               src/trackball.c)

target_link_libraries(GL_Puzzle_example
                      PRIVATE
                      m
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
