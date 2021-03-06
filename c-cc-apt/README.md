# c-cc:apt - C

Docker Image for programming language C.

## Build Image

You can manually build image by below commands.

```
$ git clone nacyot/docker-programming-languages
$ cd docker-programming-languages/c-cc-apt
$ docker build -t nacyot/c-cc:apt .
```

You can also pull image from docker hub.

```
$ docker pull -t nacyot/c-cc:apt
```

## Check version

```
$ docker run -i -t -v $(pwd):/source nacyot/c-cc:apt cc --version
cc (Ubuntu apt-19ubuntu1) 4.8.2
Copyright (C) 2013 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

## Complie Hello, World

```
$ chmod +x build.sh run.sh
$ docker run -i -t -v $(pwd):/source nacyot/c-cc:apt /source/build.sh
$ ./hello_world
Hello, World
```

## Files

### hello_world.c

```c
#include<stdio.h>

int main(void) {
  printf("Hello, World\n");
  return 0;
}

```

### build.sh

```sh
cc -o hello_world hello_world.c
```

### run.sh

```sh
/source/hello_world
```
