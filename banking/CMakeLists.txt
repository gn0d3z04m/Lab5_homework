set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(banking)

add_library(account account.h)
add_library(transaction transaction.h)

