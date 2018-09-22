cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(GLUT_Bitmap_Font_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(GLUT_Bitmap_Font_example)
target_compile_features(GLUT_Bitmap_Font_example
                        PRIVATE
                        c_std_90)

target_sources(GLUT_Bitmap_Font_example
               PRIVATE
               src/bitfont.c)

target_link_libraries(GLUT_Bitmap_Font_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
