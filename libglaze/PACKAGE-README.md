# libglaze - In memory, JSON and interface library for C++

This is a `build2` package for the [`glaze`](https://github.com/stephenberry/glaze)
C++ library. It provides an in memory, JSON and interface library for C++.


## Usage

To start using `libglaze` in your project, add the following `depends`
value to your `manifest`, adjusting the version constraint as appropriate:

```
depends: libglaze ^2.5.3
```

Then import the library in your `buildfile`:

```
import libs = libglaze%lib{glaze}
```
