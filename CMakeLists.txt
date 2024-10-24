cmake_minimum_required(VERSION 3.5.0)
project(cmakeExample VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
# include(FetchContent)
# FetchConent_Declare(
  #   fmt
  #   GIT_REPOSITORY https://github.com/fmtlib/fmt.git
  #   GIT_TAG 10.1.1 
  # )
  # FetchContent_MakeAvailable(fmt)
  
find_package(fmt CONFIG REQUIRED)

enable_testing()
  
add_executable(cmakeExample main.cpp)
  
target_link_libraries(cmakeExample PRIVATE fmt::fmt)
