ALAC
====

Apple Lossless Audio Codec with autotools. This repo uses the source
code from http://alac.macosforge.org/ and wrap it around using
autotools.

How to build
============
```
autoreconf
./configure
make
sudo make install
```

What's included
===============
* libalac, a library for ALAC en-/decoding.
* alacconvert, an example program using libalac to convert wav (in wav
or caf container) to alac (in caf container) or vice versa. It will only
build if you pass `--enable-example` to `configure`.

Documentation
=============
Either look at the .txt's in the repo or go to 
[Apple's website](http://alac.macosforge.org/).
