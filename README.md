# yolk: An event driven in-memory cache.

![Yolk image](public/yolk.png)

## Build

**Requirements:** CMake, GCC or Clang with C++23 support
```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Debug
cmake --build build
```

## Test
```bash
ctest --test-dir build --output-on-failure
```

## Run
```bash
./build/yolk
```