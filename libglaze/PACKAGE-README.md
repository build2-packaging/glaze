# Glaze

This project builds and defines the build2 package for the [Glaze](https://github.com/stephenberry/glaze) library.

The packaging code is licensed under the MIT License, the upstream artifacts are licensed under the terms and conditions of Glaze.

## Usage

You can simply add this package as dependency to your project by specifying it in your `manifest`:

```
depends: libglaze ^1.9.7
```

Then just pick the targets that you need:

```
import libs  = glaze%lib{glaze}
```
