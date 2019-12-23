# 目录
- [cmake based compilation](#cmake-based-compilation)
  * [General CMAKE commands](#general-cmake-commands)
  * [Command scenarios](#command-scenarios)
  * [Compilation flow](#compilation-flow)
  * [Issues and sulotions](#issues-and-sulotions)
- [references](#references)

# cmake based compilation

## General CMAKE commands

1. CMAKE_MINIMUM_REQUIRED
  specify the minimum required cmake version

1. PROJECT
  specify the project name

1. SET
  set a value to a variable

1. INCLUDE_DIRECTORIES
  specify the directories for head files

1. ADD_LIBRARY
  add library target

1. ADD_EXECUTABLE
  add executable target

1. TARGET_LINK_LIBRARIES
  specify libraries for specific target

1. SET_TARGET_PROPERTIES
  specify properties for specific target

1. LINK_DIRECTORIES
  https://cmake.org/cmake/help/v3.16/command/link_directories.html

1. FIND_LIBRARY
  find library with absolute path

1. FIND_PACKAGE
  find library locations with absolute path

1. INSTALL
  copy targets to specific path

## Command scenarios

1. collect source files

   a.FILE commad
      FILE(GLOB SOURCE_FILES "src/*.cpp")

## Compilation flow

[CMake Project with Third-party Dependencies](https://pmateusz.github.io/c++/cmake/2018/03/11/cmake-project-setup.html)

[How to use CMake to add Third-party Libraries to your Project](https://www.selectiveintellect.net/blog/2016/7/29/using-cmake-to-add-third-party-libraries-to-your-project-1)

++ Platform support

1. 
IF 


## Issues and sulotions

[Linking both third-party precompiled dynamic and static libaries in windows](https://stackoverflow.com/questions/38433515/linking-both-third-party-precompiled-dynamic-and-static-libaries-in-windows)
  use FIND_LIBRARY command

[cmake-cannot-find-library-using-link-directories](https://stackoverflow.com/questions/31438916/cmake-cannot-find-library-using-link-directories/31471772#31471772)

[CMAKE 修改 VS 工程属性大总结](https://blog.csdn.net/JinhuCheng/article/details/84025207)

# references
[build-a-project](https://cmake.org/cmake/help/latest/manual/cmake.1.html#build-a-project)

[cmake-variables](https://cmake.org/cmake/help/latest/manual/cmake-variables.7.html)

[FindQt4](https://cmake.org/cmake/help/latest/module/FindQt4.html#module:FindQt4)

[Useful-Variables](https://gitlab.kitware.com/cmake/community/wikis/doc/cmake/Useful-Variables)

[How-To-Write-Platform-Checks](https://gitlab.kitware.com/cmake/community/wikis/doc/tutorials/How-To-Write-Platform-Checks)

[Cmake 详解](https://blog.codekissyoung.com/%E5%B8%B8%E7%94%A8%E8%BD%AF%E4%BB%B6/cmake)
