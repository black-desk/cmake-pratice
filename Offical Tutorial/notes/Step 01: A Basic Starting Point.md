# Step 01: A Basic Starting Point

1. 一定要将 `target_include_directories(Tutorial PUBLIC "${PROJECT_BINARY_DIR}")` 放在 `add_executable(Tutorial tutorial.cxx)` 的后面, 不然会报出如下错误:

   ````
   ❯ cmake .
   -- The C compiler identification is GNU 8.3.0
   -- The CXX compiler identification is GNU 8.3.0
   -- Detecting C compiler ABI info
   -- Detecting C compiler ABI info - done
   -- Check for working C compiler: /usr/bin/cc - skipped
   -- Detecting C compile features
   -- Detecting C compile features - done
   -- Detecting CXX compiler ABI info
   -- Detecting CXX compiler ABI info - done
   -- Check for working CXX compiler: /usr/bin/c++ - skipped
   -- Detecting CXX compile features
   -- Detecting CXX compile features - done
   CMake Error at CMakeLists.txt:8 (target_include_directories):
     Cannot specify include directories for target "Tutorial" which is not built
     by this project.
   ````

2. `VERSION` 变量是大小写敏感的, 参见 [此处](https://stackoverflow.com/a/61814315/13206417)

3. 可以嵌入 Git 的 commit id 作为版本号的一部分:
   参见 [此处](https://jonathanhamberg.com/post/cmake-embedding-git-hash/) 以及本仓库中参照其做出的修改.

4. 可以通过 `set(CMAKE_EXPORT_COMPILE_COMMANDS True) `, 来导出 `compile_commands.json`

