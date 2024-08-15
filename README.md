# buildsystem-sandboxy

Graveyard of failed experiments?

This repo is just a sandbox I used to compare how to do some things with all the
different build systems, a bit of conparison and rants. Systems so far

* make
* autotools
* cmake
* bazel
* meson
* gradle
* ant
* maven
* ninja

## Make

It is possible to use make without anything else, but mostly for smaller
projects. Many other systems use it as a backend. Its scripting language is
combination of a limited shell scripting mixed with rules defining
file-dependencies and some variables. There is a whole scripting langauage
stuff hiding within make, but it's not very well known and not very portable,
probably. Make also knows a lot of things already, like how to compile C, that
is why you can make a zero line `Makefile` for trivial projects.

## Autotools

Autotools is the oldest system that is in common use still. I know it inside and
outside due to growing up in time when it was the only one. One of the reasons I
wrote this repo comparison though is that youngins these days find it too hard.
It's chock full of bad design decisions that stuck for sure but it is well
documented and has a lot of stack overflow. Supports million weird things, both
systems and concepts, like you can use some obscure architecture but also have
source code on read-only file system and build on other file system and install
on third target system. Since autotools is so old, it is based on many archaic
scripting and macro languages, like m4 and strict posix sh shell, and if I'm not
forgetting some perl to hold it together. I've also heard of guile but haven't
seen it.

## Cmake

Cmake is one of the first long-lived replacement for autotools. It's gained some
popularity but in my opinion it never really broke through. It has some
documentation and some stack overflows, but chances are some problems are not
solved by googling and some features are just missing. Cmake has its own
scripting language that doesn't really look like anything else. One of the
reasons for cmake's relative popularity is that graphical IDEs have some kind of
support for it so it's easier for beginner programmers who code using mouse and
GUIs to approach.

## Bazel

Bazel is quite ne, I think it's a google thing so probably will be discontinued
if it ever gains popularity. Its documentation mixes up C and C++ (and or it
does not support C at all except as C++), I do not have high expectations. It
has a custom scripting language. One selling point for me here is that it
promises to support large codebases with multiple languages, that may be
relevant to my interests.

First experience of bazel:

```
bazel build //main:helloc
INFO: Analyzed target //main:helloc (14 packages loaded, 57 targets configured).
INFO: Found 1 target...
[0 / 1] [Prepa] BazelWorkspaceStatusAction stable-status.txt
FATAL: bazel crashed due to an internal error. Printing stack trace:
java.lang.ExceptionInInitializerError
    at ...
Caused by: java.lang.reflect.InaccessibleObjectException: Unable to make
java.lang.String(byte[],byte) accessible: module java.base does not "opens
java.lang" to unnamed module @3e07d849
    at ...
    ... 19 more
```

literally running tutorial here!

## Meson

Meson is also one of the newer systems,  think it's been popular with gtk or
something. They have a document on porting existing autotools to meson which
does give me hope that they know what they are doing and are aware of of lots of
features autotools had, which is more than can be said of many other build tools
that claim to be better replacements. Meson seems good as a first experience so
far...

## Gradle

I only know Gradle as Android's build system for java stuff.

## Ant

Ant was the way to build java stuff in early days of java.

## Maven

Maven is probably the most popular java build system and package manager.

## Ninja

Ninja is a lower level backend like `make`?
