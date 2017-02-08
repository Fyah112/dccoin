This is the reference code for [CryptoNote](https://cryptonote.org) cryptocurrency protocol.

DCcoin

## Building DCcoin

### On *nix

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.55.

You may download them from:

* http://gcc.gnu.org/
* http://www.cmake.org/
* http://www.boost.org/
* Alternatively, it may be possible to install them using a package manager.

To build, change to a directory where this file is located, and run `make`. The resulting executables can be found in `build/release/src`.

**Advanced options:**

* Parallel build: run `make -j<number of threads>` instead of `make`.
* Debug build: run `make build-debug`.
* Test suite: run `make test-release` to run tests in addition to building. Running `make test-debug` will do the same to the debug version.
* Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++` before running `make`.

### On Windows
Dependencies: MSVC 2013 or later, CMake 2.8.6 or later, and Boost 1.55. You may download them from:

* https://www.microsoft.com/en-us/download/details.aspx?id=40784
* http://www.cmake.org/
* http://www.boost.org/

To build boost:
Download boost 1.58.0 from http://www.boost.org/
Extract files (e.g. “C:\boost_1_58_0”)
Start Visual Studio 2013 x64 command prompt (“VS2013 x64 Native Tools Command Prompt“)
Change to boost directory (e.g. “cd C:\thirdparty\vs2013\x64\boost_1_58_0”)
Execute .\bootstrap.bat
Execute b2 -j8 --toolset=msvc-14.0 address-model=64 --build-type=complete stage


To build, change to a directory where this file is located, and run theas commands:
```
mkdir build
cd build
cmake.exe -DBOOST_ROOT=C:\boost_1_58_0 -DBOOST_LIBRARYDIR=C:\boost_1_58_0\stage\lib -G "Visual Studio 14 Win64..
```

And then open in Visual studio and do Build.
Good luck!
