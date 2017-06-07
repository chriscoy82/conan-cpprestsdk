# conan-cpprestsdk

[Conan.io](https://conan.io) package for Microsoft's [C++ REST SDK](https://github.com/Microsoft/cpprestsdk)

The packages generated with this **conanfile** can be found in [conan.io](https://conan.io/source/CppRestSdk/2.9.0/BleuGamer/stable).

## Build packages

Download conan client from [Conan.io](https://conan.io) and run:

    $ python build.py

## Upload packages to server

    $ conan upload CppRestSdk/2.9.0@BleuGamer/stable --all

## Reuse the packages

### Basic setup

    $ conan install CppRestSdk/2.9.0@BleuGamer/stable

### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    CppRestSdk/2.9.0@BleuGamer/stable

    [options]
    CppRestSdk:shared=true # false

    [generators]
    cmake

Complete the installation of requirements for your project running:</small></span>

    conan install .

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.txt* and *conanbuildinfo.cmake* with all the paths and variables that you need to link with your dependencies.

### Note

Source and inspiration came from: https://github.com/ViaviSolutions/conan-cpprestsdk
Openssl update broke CppRestSdk for a lot of distros on linux, so this will build it isolated as well as many bugfixes.
