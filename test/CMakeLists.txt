add_executable(tests tests.cpp)
target_link_libraries(tests PRIVATE sdb::libsdb Catch2::Catch2WithMain)


include(CTest)


add_test(NAME "Catch2 tests" COMMAND tests)
set_tests_properties("Catch2 tests" PROPERTIES OUTPUT_ON_FAILURE TRUE)

add_subdirectory("targets")
