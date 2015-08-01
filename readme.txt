# Info 
libfontconfig was built from source with --enable-static --with-glib=no
Other libs were taken from msys2 repository
hacked the configure script of libfontconfig a bit to avoid mkstemp.

# Versions
cairo 1.14.2
fontconfig 2.11.94


# Test program
gcc -m32 test.c -o text.exe -Iinclude/cairo -Llib/i386 -lcairo -lfontconfig -lfreetype -lpng -lpixman-1 -lexpat -lharfbuzz -lbz2 -lz -lgdi32
gcc -m64 test.c -o text.exe -Iinclude/cairo -Llib/x64 -lcairo -lfontconfig -lfreetype -lpng -lpixman-1 -lexpat -lharfbuzz -lbz2 -lz -lgdi32

# Generates a PNG image
./test.exe