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

Bugs Report
===========
If you found some difficulty building it, open a new issue. Otherwise,
don't bother me. Note that I am not a programmer. So if you have any
patch regarding the sources I'm sorry I can't apply it. But if it is
about the building system, feel free to open a new  pull request or
an issue.
