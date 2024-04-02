# glaze - JSON and interface library for C++

This is a `build2` package repository for [`glaze`](https://github.com/stephenberry/glaze),
an in memory, JSON and interface library for C++.

This file contains setup instructions and other details that are more
appropriate for development rather than consumption. If you want to use
`glaze` in your `build2`-based project, then instead see the accompanying
[`PACKAGE-README.md`](libglaze/PACKAGE-README.md) file.

The development setup for `glaze` uses the standard `bdep`-based workflow.
For example:

```
git clone https://github.com/build2-packaging/glaze
cd glaze

bdep init -C @gcc cc config.cxx=g++
bdep update
bdep test
```
