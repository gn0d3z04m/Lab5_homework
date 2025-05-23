set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(banking)

add_library(account Account.h)
add_library(transaction Transaction.h)
link_libraries(account transaction)
link_libraries(transaction account)
set_target_properties(account PROPERTIES LINKER_LANGUAGE CXX)
set_target_properties(transaction PROPERTIES LINKER_LANGUAGE CXX)
