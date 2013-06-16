<!------------------------------------------------------------------------
 !Copyright (c) 2013 Tiancheng "Timothy" Gu
 !Licensed under the Apache License, Version 2.0 (the "License");
 !you may not use this file except in compliance with the License.
 !You may obtain a copy of the License at
 !
 !    http://www.apache.org/licenses/LICENSE-2.0
 !
 !Unless required by applicable law or agreed to in writing, software
 !distributed under the License is distributed on an "AS IS" BASIS,
 !WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 !See the License for the specific language governing permissions and
 !limitations under the License.
 !----------------------------------------------------------------------->

ALAC
====

Apple Lossless Audio Codec with autotools. This repo uses the source
code from http://alac.macosforge.org/ and wrap it around using
autotools and Debian build toolchain.

## Prerequisites, if you want to build it yourself

* git: to clone this repo. Optional if you are using a tarball.
* gcc: to compile stuff.
* g++: to compile stuff.
* autotools: to generate the build files.

## How to build

### Classic GNU

```bash
autoreconf -i -f
./configure
# Or if you want to
# ./configure --enable-example
make
sudo make install
```

### Debian packaging

This method works if:
* You are using a system using dpkg (like Debian, Ubuntu, etc.)
* And you want .deb's.

**I strongly suggest you to know how the Debian packaging works before
  using this method.**

1. You need to have a packaging environment.
  * If you are a maintainer or you know how to package a deb or you have
    a PPA, skip to step 3.
  * If you don't know anything about Debian packaging, go to step 2.
2. Set up packaging environment.
  * Look [here](http://www.debian.org/doc/manuals/maint-guide/start.en.html)
    for Debian users and [here](http://developer.ubuntu.com/packaging/html/getting-set-up.html)
    for Ubuntu users.
3. Edit debian/changelog.
  * Change my name to your name, and my email to your email.
  * Change raring to whatever your distro codename is.
4. Do:
   ```
   dpkg-buildpackage
   ```
5. The .deb's will be in the parent folder of the source code directory.

<!--
## Binaries

### Personal Packages Archive

If you are too lazy to download the build the sources yourself, and is
using Ubuntu or something like that, you can just install it from my PPA
at Launchpad. (I guess you know how to add a PPA to your system)

-->

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

* PPA
* `EXTRA_DIST` variable in Makefile.am's
* Visual Studio project files
