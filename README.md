CrabNet 1.001
============

Copyright (c) 2014, Oculus VR, Inc. (original RakNet)

Copyright (c) 2016-2018, TES3MP Team

Note
----
This fork is not compatible with the original RakNet.

Your compiler should support C++11.

You also need CMake 3.5 to generate project files.


PATCH APPLIED FROM SASO...
-----
patch -p1 < gcc-compile.patch


Linux
-----
```
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_POSITION_INDEPENDENT_CODE=On ..
cmake --build . -- -j4
```

Windows Build From On Linux
-------
```
mkdir build_win
cd build_win
cmake -DCMAKE_TOOLCHAIN_FILE=../XCompile.txt -DCMAKE_BUILD_TYPE=Release -DHOST=x86_64-w64-mingw32 ..
make -j 6
#cmake --build . --target RakNetLibStatic
#                --config Release \
#                --clean-first
```
