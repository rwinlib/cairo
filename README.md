# Cairo 

This branch is a built of cairo 1.16.0 _without fontconfig_. It uses the native Windows font api. See [PKGBUILD](PKGBUILD) file.

Link in this order:

```
 -lcairo -lpixman-1 -lfreetype -lbz2 -lharfbuzz -lm -lpng -lz \
   -lgdi32 -lmsimg32
```
