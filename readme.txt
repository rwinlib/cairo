# Info 
libfontconfig was built from source using: --enable-static --enable-iconv
hacked the configure script of libfontconfig a bit to avoid mkstemp
Other libs were taken from msys2 repository


# Versions
cairo 1.14.2
fontconfig 2.11.94
freetype 2.6
png 1.6.17
pixman 0.32.6
expat 2.1.0
harfbuzz 0.9.41
bzip2 1.0.6
zlib 1.2.8

# Test program
gcc -m32 test.c -o test.exe -Iinclude/cairo -Llib/i386 -lcairo -lfontconfig -lfreetype -lpng -lpixman-1 -lexpat -lharfbuzz -lbz2 -lz -lgdi32
gcc -m64 test.c -o test.exe -Iinclude/cairo -Llib/x64 -lcairo -lfontconfig -lfreetype -lpng -lpixman-1 -lexpat -lharfbuzz -lbz2 -lz -lgdi32

# Generates a PNG image
./test.exe
