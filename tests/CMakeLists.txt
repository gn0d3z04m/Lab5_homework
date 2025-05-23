set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(tests)

file(GLOB TEST_SOURCES *.cpp)
add_executable(check \${TEST_SOURCES})
target_link_libraries(check \${PROJECT_NAME} gtest_main)
add_test(NAME check COMMAND check)
