## LLVM for Fortran support in RAPTOR

This LLVM fork contains patches that enable RAPTOR to work with Fortran code. It is not required for C or C++ support.


### Building
To build, follow the instruction i
Consult the
[Getting Started with LLVM](https://llvm.org/docs/GettingStarted.html#getting-the-source-code-and-building-llvm)
page for information on building and running LLVM.

A possible sequence of commands to build this is the following.
``` shell
cmake --fresh -DCMAKE_BUILD_TYPE=Release \
  -DCMAKE_INSTALL_PREFIX=${BASE_DIR}/llvm-install \
  -DLLVM_ENABLE_PROJECTS="clang;flang;lld;openmp" \
  -S llvm -B build -G Ninja
ninja -C ./build install
```
