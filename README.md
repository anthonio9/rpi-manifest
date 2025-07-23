# rpi-manifest

Yocto has layers, like Ogres and onions. Put them layers together.

## Install the `repo` utility:

To use this manifest repo, the `repo` tool must be installed first.

```sh
mkdir ~/bin
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo  > ~/bin/repo
chmod a+x ~/bin/repo
PATH=${PATH}:~/bin
```

## Install essential host packages

Your Build Host must install required packages for the Yocto build.
Reference to the section "Build Host Packages" in the document ["Yocto Project Quick build"](https://docs.yoctoproject.org/5.1.2/brief-yoctoprojectqs/index.html#build-host-packages).

## Download the RPI Yocto resources

```sh
mkdir rpi-scarthgap
cd rpi-scarthgap
repo init -u https://github.com/anthonio9/rpi-manifest -b scarthgap -m rpi-6.12.25.xml
repo sync
```

Enjoy your new Yocto environment!

