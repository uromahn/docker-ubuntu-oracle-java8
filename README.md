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

## Image with Unlimited Strength JCE

By default the Oracle 8 JDK/JRE comes with limited strength encryption (JCE). To remove this limitation
you can download and install new policy files from Oracle's site. However, those files cannot be
included into this project.
In order to build an image with unlimted strength JCE you will have to do the following:

1. download the corresponding policy files from here: http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html
2. unzip the archive into this folder - this will create a folder called 'UnlimitedJCEPolicyJDK8'
3. build an image with the command:
```
$ docker build -t ubuntu-oracle-java8 -f Dockerfile.unlimitedJCE .
```
This will result in an image with unlimited strength encryption.
