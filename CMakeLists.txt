cmake_minimum_required(VERSION 3.4)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(bank_lib)

add_library(account_lib STATIC ${CMAKE_CURRENT_SOURCE_DIR}/Account.cpp)
add_library(transaction_lib STATIC ${CMAKE_CURRENT_SOURCE_DIR}/Transaction.cpp)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(transaction_lib account_lib)
set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/third-party/CMake-codecov/cmake" ${CMAKE_MODULE_PATH})