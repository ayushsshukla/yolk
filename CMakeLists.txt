cmake_minimum_required(VERSION 3.24)

project(yolk
        VERSION 0.1.0
        DESCRIPTION "An event driven in-memory cache"
        LANGUAGES CXX
)

add_executable(yolk
    src/main.cpp
)

set_target_properties(yolk PROPERTIES
        CXX_STANDARD 23
        CXX_STANDARD_REQUIRED YES
        CXX_EXTENSIONS NO
)

target_compile_options(yolk PRIVATE
    -Wall -Wextra -Wpedantic -Wconversion -Wshadow
)

include(CTest)

if(BUILD_TESTING)
    add_test(
            NAME yolk_smoke
            COMMAND yolk
    )
endif ()