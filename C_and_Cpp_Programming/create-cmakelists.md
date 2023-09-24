# Create a CMakeLists.txt file

You can do this manually if you wish to do so.  This usually is in the root directory/folder of your project.

The first line of the file must be:

`cmake_minimum_required(VERSION 3.16)`

The next line must be `project(my_project)`

```cmake
cmake_minimum_required(VERSION 3.10)

project(myproject)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(myprogram main.cpp foo.cpp bar.cpp)
```
