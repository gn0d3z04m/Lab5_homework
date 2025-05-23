set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(banking)

add_library(account Account.h)
add_library(transaction Transaction.h)
link_libraries(account transation)
link_libraries(transation account)
