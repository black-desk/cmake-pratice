# Step 4: Installing and Testing

## Install Rules

1. [from](https://stackoverflow.com/a/44649542/13206417) 卸载由 cmake 安装的文件的方法

   > If you want to add an **uninstall** target you can take a look to the official **CMake FAQ** at:
   >
   > > https://gitlab.kitware.com/cmake/community/wikis/FAQ#can-i-do-make-uninstall-with-cmake
   >
   > If you just want a quick way to uninstall all files, just run:
   >
   > ```
   > xargs rm < install_manifest.txt
   > ```
   >
   > `install_manifest.txt` file is created when you run `make install`.

## Testing Support

