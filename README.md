ALAC
====

Apple Lossless Audio Codec with autotools. This repo uses the source
code from http://alac.macosforge.org/ and wrap it around using
autotools.

## How to build

* Method No. 1: Classic GNU

```
autoreconf
./configure
make
sudo make install
```

* **Unstable** method No. 2: Work with `dpkg`.

```
dpkg-buildpackage
```

## What's included

* libalac, a library for ALAC en-/decoding.
* alacconvert, an example program using libalac to convert wav (in wav
or caf container) to alac (in caf container) or vice versa. It will only
build if you pass `--enable-example` to `configure`.

## Documentation
### `alacconvert`
Look at the man page.

### The library
Either look at the .txt's in the repo or go to 
[Apple's website](http://alac.macosforge.org/).

## Bugs Report

If you found some difficulty building it, open a new issue. Otherwise,
don't bother me. Note that I am not a programmer. So if you have any
patch regarding the sources I'm sorry I can't apply it. But if it is
about the building system, feel free to open a new  pull request or
an issue.

## Authors

* debian/&#42;, Makefile.am, &#42;/Makefile.am, alac.pc.in,
alacconvert.1, configure.ac, README.md:
**Tiancheng "Timothy" Gu**

* The rest: **Apple Inc.**

## To-do

* Complete & working Debian build toolchain
* `EXTRA_DIST` variable in Makefile.am's
* Visual Studio project files

## Copyright of this file

Copyright (c) 2013 Tiancheng "Timothy" Gu
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.