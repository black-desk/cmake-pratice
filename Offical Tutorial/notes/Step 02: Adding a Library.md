# Step 2: Adding a Library

1. `add_library()` `add_executable()` 这些命令实际上指的是 "在我们项目的 **构建目标** 中加上一个 库/可执行 文件".

2. `add_subdirectory()` 命令用来包含子目录, 这个子目录需要有一个 CMakeLists.txt 

3. `target_include_directories()` 命令中的 `PUBLIC` 含意如下, 主要是用来设置一些变量的. 

   > The INTERFACE, PUBLIC and PRIVATE keywords are required to specify the scope of the following arguments. PRIVATE and PUBLIC items will populate the INCLUDE_DIRECTORIES property of <target>. PUBLIC and INTERFACE items will populate the INTERFACE_INCLUDE_DIRECTORIES property of <target>. The following arguments specify include directories.

