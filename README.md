# submodule-test

## Description

This repository is a test of using [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) within a Particle project.

I added [my port of libfixmath](https://github.com/nrobinson2000/libfixmath) to this project with the following commands.

```bash
$ git init # Particle projects do not start as git repos
$ mkdir lib
$ cd lib
$ git submodule add https://github.com/nrobinson2000/libfixmath
```

After that, I copied [the example](https://github.com/nrobinson2000/libfixmath/blob/master/examples/unittests/unittests.ino) into the project.

I am able to compile the project using Particle Workbench or po-util.

## Building this project

Here are the neccesary commands for cloning this project and submodules, as well as compiling the project with po-util:

```bash
$ git clone --recurse-submodules https://github.com/nrobinson2000/submodule-test
$ po photon build-beta
```