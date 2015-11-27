# Ubuntu 14.04 (Trusty) Docker Container with Oracle's Java 8 SDK

This Dockerfile will create a basic container with Ubuntu 14.04 (Trusty) and installs Oracle's Java 8 SDK into it.

To install Oracle's Java 8 SDK, it will use the webupd8team Debian ppa.

## How to use?

Clone this repository and simply type:

```
$ docker build -t ubuntu-oracle-java8 .
```

If you prefer a different tag for your image, then simply replace `ubuntu-oracle-java8` with your preferred one.

## Prerequisites

You will have to have Docker installed on your local machine.

This Dockerfile should work with all Docker versions but I highly recommend to use the latest version for it.
