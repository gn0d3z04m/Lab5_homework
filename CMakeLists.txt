set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
cmake_minimum_required(VERSION 3.4)

project(lab5)

include_directories("banking/" "tests/" "third-party/gtest" "third-party")

add_subdirectory(banking)
add_subdirectory(tests)

if(BUILD_TESTS)
  enable_testing()
  add_subdirectory(third-party/gtest)
  target_link_libraries(check_acc gtest gtest_main)
  target_link_libraries(check_tr gtest gtest_main)
endif()
