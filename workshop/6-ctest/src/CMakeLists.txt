cmake_minimum_required(VERSION 3.25)
project(TestExample LANGUAGES CXX)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_library(bank bank.cpp)
target_include_directories(bank PUBLIC ${TestExample_SOURCE_DIR}/include)

add_executable(test_bank test_bank.cpp)
target_link_libraries(test_bank PRIVATE bank)


enable_testing()
add_test(
    NAME test_bank
    COMMAND $<TARGET_FILE:test_bank>
)
