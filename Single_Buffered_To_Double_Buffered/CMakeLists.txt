cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(Single_Buffered_To_Double_Buffered_example)

find_package(GLUT REQUIRED)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)


add_executable(Single_Buffered_To_Double_Buffered_example)
target_compile_features(Single_Buffered_To_Double_Buffered_example
                        PRIVATE
                        c_std_90)

target_sources(Single_Buffered_To_Double_Buffered_example
               PRIVATE
               src/sb2db.c)

target_link_libraries(Single_Buffered_To_Double_Buffered_example
                      PRIVATE
                      GLUT::GLUT
                      OpenGL::GLU
                      OpenGL::GL)
