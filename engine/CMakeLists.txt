add_executable(linfer
    main.cpp
)

target_compile_options(linfer PRIVATE
    -Wall -Wextra -Wpedantic
)
