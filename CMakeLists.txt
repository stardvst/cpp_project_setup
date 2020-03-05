cmake_minimum_required(VERSION 3.9.2)

add_executable(intro main.cpp)

if (MSVC)
	add_compile_options(/W4)
else()
	add_compile_options(-Wall -Wextra -pedantic)
endif()

enable_testing()
add_executable(tester tester.cpp)
add_test(Tester tester)
