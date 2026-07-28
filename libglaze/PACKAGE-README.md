# libglaze - In memory, JSON and interface library for C++

This is a `build2` package for the [`glaze`](https://github.com/stephenberry/glaze)
C++ library. It provides an in memory, JSON and interface library for C++.


## Usage

To start using `libglaze` in your project, add the following `depends`
value to your `manifest`, adjusting the version constraint as appropriate:

```
depends: libglaze ^ 7.9.1
```

Then import the library in your `buildfile`:

```
import libs = libglaze%lib{glaze}
```


## Configuration variables

This package provides the following configuration variables:

```
[bool] config.libglaze.repe_rpc                  ?= true
[bool] config.libglaze.disable_always_inline     ?= false
[bool] config.libglaze.default_optimization_size ?= false
[bool] config.libglaze.disable_simd              ?= false
```

`config.libglaze.repe_rpc` \
Enables the RPC-over-reflection feature and pulls in `libasio` as a
dependency. Disable it to drop the Asio dependency when RPC support is not
needed.

`config.libglaze.disable_always_inline` (`GLZ_DISABLE_ALWAYS_INLINE`) \
Suppresses glaze's aggressive `always_inline` annotations. Useful when
compiling with sanitizers or toolchains that have trouble with forced inlining.
The define is re-exported to consumers so headers and the binary stay
consistent.

`config.libglaze.default_optimization_size` (`GLZ_DEFAULT_OPTIMIZATION_SIZE`) \
Switches glaze's internal optimization strategy to prefer smaller code over
faster code. Reduces binary size at the cost of some throughput. The define is
re-exported to consumers so headers and the binary stay consistent.

`config.libglaze.disable_simd` (`GLZ_DISABLE_SIMD`) \
Builds the scalar fallback path instead of SIMD-accelerated parsing and
serialization. Slower. The define is re-exported to consumers so headers and
the binary stay consistent.
