# libglaze - Extremely fast, in memory, JSON and interface library for modern C++

This is a `build2` package for the [`glaze`](https://github.com/stephenberry/glaze)
C++ library. It provides an extremely fast, in memory, JSON and interface library for modern C++.


## Usage

To start using `libglaze` in your project, add the following `depends`
value to your `manifest`, adjusting the version constraint as appropriate:

```
depends: libglaze ^2.4.0
```

Then import the library in your `buildfile`:

```
import libs = libglaze%lib{glaze}
```
