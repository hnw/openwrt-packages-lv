# openwrt-packages-lv [![Build Status](https://secure.travis-ci.org/hnw/openwrt-packages-lv.svg?branch=master)](https://travis-ci.org/hnw/openwrt-packages-lv)

This is [lv](https://web.archive.org/web/20071209063452/http://www.ff.iij4u.or.jp:80/~nrt/lv/index.html) package for OpenWrt, tested on OpenWrt 15.05.1 / LEDE 17.01.4.

# How to install binary package

See [hnw/openwrt-packages](https://github.com/hnw/openwrt-packages).

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot:

```
$ cp feeds.conf.default feeds.conf # if needed
$ echo 'src-git hnw_lv https://github.com/hnw/openwrt-packages-lv.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install lv
$ make defconfig
$ make package/toolchain/compile
$ make package/lv/compile
```
