add_subdirectory(external/doctest)

add_executable(constexpr_md5_unit_tests main.cc)

target_compile_features(constexpr_md5_unit_tests
    PRIVATE
        cxx_std_17
)

target_link_libraries(constexpr_md5_unit_tests
    PRIVATE
        doctest::doctest
        constexpr_md5
)

add_test(unit_tests constexpr_md5_unit_tests)
