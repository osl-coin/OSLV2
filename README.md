## Oscillate Network

Copyright (c) 2018-2019 The Oscillate Network.
Copyright (c) 2018-2019 The Arqma Network.
Copyright (c) 2014-2018 The Monero Project.  
Portions Copyright (c) 2012-2013 The Cryptonote developers.

## Development resources

- Web: [oscillate.com](https://oscillate.com)
- Mail: [support@oscillate.com](mailto:support@oscillate.com)
- GitHub: [https://github.com/oscillate/oscillate](https://github.com/oscillate/oscillate)
- Discord: [https://discord.gg/TqXZWGm](https://discord.gg/TqXZWGm)
- Telegram: [https://t.me/joinchat/HNpOMRIiNSoCn0zYrAOofw](https://t.me/joinchat/HNpOMRIiNSoCn0zYrAOofw)

## Other Oscillate related websites

- Oscillate Information Centre: [https://oscillate.github.io](https://oscillate.github.io)
- Oscillate Blockchain Explorer: [blockexplorer.oscillate.com](https://blockexplorer.oscillate.com)
- Oscillate Blockchain Raw File updated every 24hrs: [https://raw.oscillate.com](https://raw.oscillate.com)
- Oscillate BitcoinTalk Thread: [https://bitcointalk.org/index.php?topic=4474605.0](https://bitcointalk.org/index.php?topic=4474605.0)
- Oscillate Mining Pools List: [https://pools.oscillate.com](https://pools.oscillate.com)
- Oscillate Mining Pools Stream: [https://miningpoolstats.stream/oscillate](https://miningpoolstats.stream/oscillate)
- Oscillate Payment Gateway: [https://pg.oscillate.com](https://pg.oscillate.com)
- Oscillate WooCommerce Payment Plugin: [https://github.com/oscillate/oscillate-payments-woocommerce-gateway](https://github.com/oscillate/oscillate-payments-woocommerce-gateway)
- Oscillate Off-line Wallet Address Generator: [https://generate.oscillate.com](https://generate.oscillate.com)
- myOscillate - Oscillate Web-Wallet Interface: [https://myoscillate.com](https://myoscillate.com)
- oscillateDroid - Oscillate Android Wallet: [https://play.google.com/store/apps/details?id=com.oscillate.Droid](https://play.google.com/store/apps/details?id=com.oscillate.Droid)

## Oscillate Social-Media Websites

- Twitter: [https://twitter.com/ArQmA_Network](https://twitter.com/ArQmA_Network)
- FaceBook: [https://www.facebook.com/OSCILLATEnetwork](https://www.facebook.com/OSCILLATEnetwork)
- Medium: [https://medium.com/@ArQmANetwork](https://medium.com/@ArQmANetwork)
- YouTube: [https://www.youtube.com/channel/UC24ZbH8J1SKpxmdakIJotoA](https://www.youtube.com/channel/UC24ZbH8J1SKpxmdakIJotoA)

## Oscillate Exchange Websites

- TradeOgre: [https://tradeogre.com/exchange/BTC-ARQ](https://tradeogre.com/exchange/BTC-ARQ)
- Crex24: [https://crex24.com/exchange/ARQ-BTC](https://crex24.com/exchange/ARQ-BTC)

## Introduction

Oscillate is a private, secure, untraceable, decentralised digital currency. You are your bank, you control your funds, and nobody can trace your transfers unless you allow them to do so.

**Privacy:** Oscillate uses a cryptographically sound system to allow you to send and receive funds without your transactions being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain absolutely private by default.

**Security:** Using the power of a distributed peer-to-peer consensus network, every transaction on the network is cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Untraceability:** By taking advantage of ring signatures, a special property of a certain type of cryptography, Oscillate is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.

## SSL

As a network, Oscillate supports complete, cryptographically secured connections at all levels. This includes, but is not limited to Oscillate Network Nodes (Full nodes), Remote Nodes and all wallets - CLI and GUI for desktop, and Android and iOS [ iOS is under development].    

Oscillate Network will be consistently implementing the highest security protocols to achieve the greatest privacy for all transactions, as well as all communications made over the Oscillate Network.

The use of SSL connections means that there will not be any possibility to use the Oscillate Network with unsecured or tampered connections (daemons), and that your privacy will remain a feature built in a protocol level.

 * Below is an example how to generate SSL Keys with openssl

    `$ openssl genrsa -out /tmp/KEY 4096`    
    `$ openssl req -new -key /tmp/KEY -out /tmp/REQ`    
    `$ openssl x509 -req -days 999999 -sha256 -in /tmp/REQ -signkey /tmp/KEY -out /tmp/CERT`    

 * Above example will generate 4096bit SSL Cert at /tmp (which can be changed)*


## About this project

This is the core implementation of Oscillate. It is open source and completely free to use without restrictions, except for those specified in the license agreement below. There are no restrictions on anyone creating an alternative implementation of Oscillate that uses the protocol and network in a compatible manner.

As with many development projects, the repository on Github is considered to be the "staging" area for the latest changes. Before changes are merged into that branch on the main repository, they are tested by individual developers in their own branches, submitted as a pull request, and then subsequently tested by contributors who focus on testing and code reviews. That having been said, the repository should be carefully considered before using it in a production environment, unless there is a patch in the repository for a particular show-stopping issue you are experiencing. It is generally a better idea to use a tagged release for stability.

**Anyone is welcome to contribute to Oscillate's codebase!** If you have a fix or code change, feel free to submit it as a pull request directly to the "master" branch. In cases where the change is relatively small or does not affect other parts of the codebase it may be merged in immediately by any one of the collaborators. On the other hand, if the change is particularly large or complex, it is expected that it will be discussed at length either well in advance of the pull request being submitted, or even directly on the pull request.

## License

See [LICENSE](LICENSE).

## Contributing

If you want to help out, see [CONTRIBUTING](CONTRIBUTING.md) for a set of guidelines.

## Compiling Oscillate from source

## Build

### IMPORTANT

That build is from the master branch, which is used for active development and can be either unstable or incompatible with release software. Please compile release branches.

Status (branch: master): [![Build Status](https://travis-ci.org/oscillate/oscillate.svg?branch=master)](https://travis-ci.org/oscillate/oscillate)


### Dependencies

The following table summarizes the tools and libraries required to build. A
few of the libraries are also included in this repository (marked as
"Vendored"). By default, the build uses the library installed on the system,
and ignores the vendored sources. However, if no library is found installed on
the system, then the vendored source will be built and used. The vendored
sources are also used for statically-linked builds because distribution
packages often include only shared library binaries (`.so`) but not static
library archives (`.a`).

| Dep          | Min. version  | Vendored | Debian/Ubuntu pkg  | Arch pkg     | Fedora            | Optional | Purpose        |
| ------------ | ------------- | -------- | ------------------ | ------------ | ----------------- | -------- | -------------- |
| GCC          | 7.3.0         | NO       | `build-essential`  | `base-devel` | `gcc`             | NO       |                |
| CMake        | 3.6.3         | NO       | `cmake`            | `cmake`      | `cmake`           | NO       |                |
| pkg-config   | any           | NO       | `pkg-config`       | `base-devel` | `pkgconf`         | NO       |                |
| Boost        | 1.62          | NO       | `libboost-all-dev` | `boost`      | `boost-devel`     | NO       | C++ libraries  |
| OpenSSL      | basically any | NO       | `libssl-dev`       | `openssl`    | `openssl-devel`   | NO       | sha256 sum     |
| libzmq       | 3.0.0         | NO       | `libzmq3-dev`      | `zeromq`     | `cppzmq-devel`    | NO       | ZeroMQ library |
| OpenPGM      | ????          | NO       | `libpgm-dev`       | `libpgm`     | `openpgm-devel`   | NO       | For ZeroMQ     |
| libnorm[2]   | ?             | NO       | `libnorm-dev`      |              |               `   | YES      | For ZeroMQ     |
| libunbound   | 1.4.16        | YES      | `libunbound-dev`   | `unbound`    | `unbound-devel`   | NO       | DNS resolver   |
| libsodium    | ?             | NO       | `libsodium-dev`    | ?            | `libsodium-devel` | NO       | Cryptography   |
| libunwind    | any           | NO       | `libunwind8-dev`   | `libunwind`  | `libunwind-devel` | YES      | Stack traces   |
| liblzma      | any           | NO       | `liblzma-dev`      | `xz`         | `xz-devel`        | YES      | For libunwind  |
| libreadline  | 6.3.0         | NO       | `libreadline6-dev` | `readline`   | `readline-devel`  | YES      | Input editing  |
| ldns         | 1.6.17        | NO       | `libldns-dev`      | `ldns`       | `ldns-devel`      | YES      | SSL toolkit    |
| expat        | 1.1           | NO       | `libexpat1-dev`    | `expat`      | `expat-devel`     | YES      | XML parsing    |
| GTest        | 1.5           | YES      | `libgtest-dev`[1]  | `gtest`      | `gtest-devel`     | YES      | Test suite     |
| Doxygen      | any           | NO       | `doxygen`          | `doxygen`    | `doxygen`         | YES      | Documentation  |
| Graphviz     | any           | NO       | `graphviz`         | `graphviz`   | `graphviz`        | YES      | Documentation  |
| HIDAPI       | ?             | NO       | `libhidapi-dev`    | ``           | ``                | NO       | for Device     |
| libusb-1.0   | 1.0           | NO       | `libusb-1.0-0-dev` | ``           | ``                | NO       |                |
| libudev      | ?             | NO       | `libudev-dev`      | ``           | ``                | NO       |                |
| protobuf     | ?             | NO       | `protobuf-compiler`| ``           | ``                | NO       | serializing    |
|              |               |          | `libprotobuf-dev`  | ``           | ``                |          | structured data|
-------------------------------------------------------------------------------------------------------------------------------


[1] On Debian/Ubuntu `libgtest-dev` only includes sources and headers. You must
build the library binary manually. This can be done with the following command ```sudo apt-get install libgtest-dev && cd /usr/src/gtest && sudo cmake . && sudo make && sudo mv libg* /usr/lib/ ```
[2] libnorm-dev is needed if your zmq library was built with libnorm, and not needed otherwise

Debian / Ubuntu one liner for all dependencies

``` sudo apt update && sudo apt install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libunwind8-dev liblzma-dev libreadline6-dev libldns-dev libexpat1-dev doxygen graphviz libpgm-dev libudev-dev libusb-1.0-0-dev libhidapi-dev protobuf-compiler libprotobuf-dev xsltproc gperf autoconf automake libtool-bin libprotobuf-c-dev ```

Install all dependencies at once on OSX:

``` brew update && brew install cmake pkg-config boost zmq libpgm unbound libsodium miniupnpc libunwind-headers xz readline ldns expat doxygen graphviz protobuf ```

### Cloning the repository

Clone recursively to pull-in needed submodule(s):

`$ git clone https://github.com/oscillate/oscillate`

If you already have a repo cloned, initialize and update:

`$ cd oscillate && git checkout release-v0.5.1`    
`$ git submodule init && git submodule update`    

### Build instructions

Oscillate uses the CMake build system and a top-level [Makefile](Makefile) that
invokes cmake commands as needed.

#### On Linux and OS X

* Install the dependencies
* Change to the root of the source code directory and build:

        `$ cd oscillate && make`


    *Optional*: If your machine has several cores and enough memory, enable
    parallel build by running `make -j<number of threads>` instead of `make`. For
    this to be worthwhile, the machine should have one core and about 2GB of RAM
    available per thread.

    *Note*: If cmake can not find zmq.hpp file on OS X, installing `zmq.hpp` from
    https://github.com/zeromq/cppzmq to `/usr/local/include` should fix that error.

* The resulting executables can be found in `build/release/bin`

* Add `PATH="$PATH:$HOME/oscillate/build/release/bin"` to `.profile`

* Run Oscillate with `oscillated --detach`

* **Optional**: build and run the test suite to verify the binaries:

        make release-test

    *NOTE*: `core_tests` test may take a few hours to complete.

* **Optional**: to build binaries suitable for debugging:

         make debug

* **Optional**: to build statically-linked binaries:

         make release-static

Dependencies need to be built with -fPIC. Static libraries usually aren't, so you may have to build them yourself with -fPIC. Refer to their documentation for how to build them.

* **Optional**: build documentation in `doc/html` (omit `HAVE_DOT=YES` if `graphviz` is not installed):

        HAVE_DOT=YES doxygen Doxyfile

#### On the Raspberry Pi

Tested on a Raspberry Pi Zero with a clean install of minimal Raspbian Stretch (2017-09-07 or later) from https://www.raspberrypi.org/downloads/raspbian/. If you are using Raspian Jessie, [please see note in the following section](#note-for-raspbian-jessie-users).

* `apt-get update && apt-get upgrade` to install all of the latest software

* Install the dependencies for Oscillate from the 'Debian' column in the table above.

* Increase the system swap size:
```
	sudo /etc/init.d/dphys-swapfile stop  
	sudo nano /etc/dphys-swapfile  
	CONF_SWAPSIZE=1024  
	sudo /etc/init.d/dphys-swapfile start  
```
* Clone oscillate and checkout most recent release version:
```
  git clone https://github.com/oscillate/oscillate.git
	cd oscillate

```
* Build:
```
  make release
```
* Wait 4-6 hours

* The resulting executables can be found in `/build/Linux/master/release/binn`

* Add `PATH="$PATH:$HOME/oscillate/build/Linux/master/release/bin"` to `.profile`

* Run Oscillate with `oscillated --detach`

* You may wish to reduce the size of the swap file after the build has finished, and delete the boost directory from your home directory

#### *Note for Raspbian Jessie users:*

If you are using the older Raspbian Jessie image, compiling Oscillate is a bit more complicated. The version of Boost available in the Debian Jessie repositories is too old to use with Oscillate, and thus you must compile a newer version yourself. The following explains the extra steps, and has been tested on a Raspberry Pi 2 with a clean install of minimal Raspbian Jessie.

* As before, `apt-get update && apt-get upgrade` to install all of the latest software, and increase the system swap size

```
	sudo /etc/init.d/dphys-swapfile stop  
	sudo nano /etc/dphys-swapfile  
	CONF_SWAPSIZE=1024  
	sudo /etc/init.d/dphys-swapfile start  
```

* Then, install the dependencies for Oscillate except `libunwind` and `libboost-all-dev`

* Install the latest version of boost (this may first require invoking `apt-get remove --purge libboost*` to remove a previous version if you're not using a clean install):
```
	cd  
	wget https://sourceforge.net/projects/boost/files/boost/1.68.0/boost_1_68_0.tar.bz2  
	tar xvfo boost_1_68_0.tar.bz2  
	cd boost_1_68_0  
	./bootstrap.sh  
	sudo ./b2  
```
* Wait ~8 hours
```
	sudo ./bjam install
```
* Wait ~4 hours

* From here, follow the [general Raspberry Pi instructions](#on-the-raspberry-pi) from the "Clone oscillate and checkout most recent release version" step.

#### On Windows:

Binaries for Windows are built on Windows using the MinGW toolchain within
[MSYS2 environment](http://msys2.github.io). The MSYS2 environment emulates a
POSIX system. The toolchain runs within the environment and *cross-compiles*
binaries that can run outside of the environment as a regular Windows
application.

**Preparing the build environment**

1. Download and install the [MSYS2 installer](http://msys2.github.io).

2. Open the MSYS shell via the `MSYS2 MSYS` shortcut at Menu Start

3. Update packages using pacman:  

        pacman -Syu    

4. Exit the MSYS shell using Alt+F4 or by clicking X at top-right corner. It is Very Important to do not exit to shell!!.

5. Start `MSYS2 MINGW64` from Menu Start

6. Update packages again using pacman:  

        pacman -Syu    

7. Install dependencies:

    To build for 64-bit Windows:

        pacman -S git mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-zeromq mingw-w64-x86_64-libsodium mingw-w64-x86_64-hidapi protobuf-devel mingw-w64-x86_64-protobuf-c mingw-w64-x86_64-protobuf

**Building**

* Download Oscillate with command:

	`git clone https://github.com/oscillate/oscillate`

* Change branch to last Release:

	`cd oscillate && git checkout release-v0.5.1`    

* Activate and update submodules:

  `git submodule init && git submodule update`

* If you are on a 64-bit system, run:

        make release-static-win

* The resulting executables can be found in `build/release/bin`

* **Optional**: to build Windows binaries suitable for debugging on a 64-bit system, run:

        make debug-static-win

* The resulting executables can be found in `build/debug/bin`

*** Oscillate does Not support 32-bit Windows anymore ***

### On FreeBSD:

The project can be built from scratch by following instructions for Linux above. If you are running oscillate in a jail you need to add the flag: `allow.sysvipc=1` to your jail configuration, otherwise lmdb will throw the error message: `Failed to open lmdb environment: Function not implemented`.

We expect to add Oscillate into the ports tree in the near future, which will aid in managing installations using ports or packages.

### On OpenBSD:

#### OpenBSD < 6.2

This has been tested on OpenBSD 5.8.

You will need to add a few packages to your system. `pkg_add db cmake gcc gcc-libs g++ miniupnpc gtest`.

The doxygen and graphviz packages are optional and require the xbase set.

The Boost package has a bug that will prevent librpc.a from building correctly. In order to fix this, you will have to Build boost yourself from scratch. Follow the directions here (under "Building Boost"):
https://github.com/bitcoin/bitcoin/blob/master/doc/build-openbsd.md

You will have to add the serialization, date_time, and regex modules to Boost when building as they are needed by Oscillate.

To build: `env CC=egcc CXX=eg++ CPP=ecpp DEVELOPER_LOCAL_TOOLS=1 BOOST_ROOT=/path/to/the/boost/you/built make release-static-64`

#### OpenBSD >= 6.2

You will need to add a few packages to your system. `pkg_add cmake miniupnpc zeromq libiconv`.

The doxygen and graphviz packages are optional and require the xbase set.


Build the Boost library using clang. This guide is derived from: https://github.com/bitcoin/bitcoin/blob/master/doc/build-openbsd.md

We assume you are compiling with a non-root user and you have `doas` enabled.

Note: do not use the boost package provided by OpenBSD, as we are installing boost to `/usr/local`.

```
# Create boost building directory
mkdir ~/boost
cd ~/boost

# Fetch boost source
ftp -o boost_1_64_0.tar.bz2 https://netcologne.dl.sourceforge.net/project/boost/boost/1.64.0/boost_1_64_0.tar.bz2

# MUST output: (SHA256) boost_1_64_0.tar.bz2: OK
echo "7bcc5caace97baa948931d712ea5f37038dbb1c5d89b43ad4def4ed7cb683332 boost_1_64_0.tar.bz2" | sha256 -c
tar xfj boost_1_64_0.tar.bz2

# Fetch and apply boost patches, required for OpenBSD
ftp -o boost_test_impl_execution_monitor_ipp.patch https://raw.githubusercontent.com/openbsd/ports/bee9e6df517077a7269ff0dfd57995f5c6a10379/devel/boost/patches/patch-boost_test_impl_execution_monitor_ipp
ftp -o boost_config_platform_bsd_hpp.patch https://raw.githubusercontent.com/openbsd/ports/90658284fb786f5a60dd9d6e8d14500c167bdaa0/devel/boost/patches/patch-boost_config_platform_bsd_hpp

# MUST output: (SHA256) boost_config_platform_bsd_hpp.patch: OK
echo "1f5e59d1154f16ee1e0cc169395f30d5e7d22a5bd9f86358f738b0ccaea5e51d boost_config_platform_bsd_hpp.patch" | sha256 -c
# MUST output: (SHA256) boost_test_impl_execution_monitor_ipp.patch: OK
echo "30cec182a1437d40c3e0bd9a866ab5ddc1400a56185b7e671bb3782634ed0206 boost_test_impl_execution_monitor_ipp.patch" | sha256 -c

cd boost_1_64_0
patch -p0 < ../boost_test_impl_execution_monitor_ipp.patch
patch -p0 < ../boost_config_platform_bsd_hpp.patch

# Start building boost
echo 'using clang : : c++ : <cxxflags>"-fvisibility=hidden -fPIC" <linkflags>"" <archiver>"ar" <striper>"strip"  <ranlib>"ranlib" <rc>"" : ;' > user-config.jam
./bootstrap.sh --without-icu --with-libraries=chrono,filesystem,program_options,system,thread,test,date_time,regex,serialization,locale --with-toolset=clang
./b2 toolset=clang cxxflags="-stdlib=libc++" linkflags="-stdlib=libc++" -sICONV_PATH=/usr/local
doas ./b2 -d0 runtime-link=shared threadapi=pthread threading=multi link=static variant=release --layout=tagged --build-type=complete --user-config=user-config.jam -sNO_BZIP2=1 -sICONV_PATH=/usr/local --prefix=/usr/local install
```

Build cppzmq

Build the cppzmq bindings.

We assume you are compiling with a non-root user and you have `doas` enabled.

```
# Create cppzmq building directory
mkdir ~/cppzmq
cd ~/cppzmq

# Fetch cppzmq source
ftp -o cppzmq-4.2.3.tar.gz https://github.com/zeromq/cppzmq/archive/v4.2.3.tar.gz

# MUST output: (SHA256) cppzmq-4.2.3.tar.gz: OK
echo "3e6b57bf49115f4ae893b1ff7848ead7267013087dc7be1ab27636a97144d373 cppzmq-4.2.3.tar.gz" | sha256 -c
tar xfz cppzmq-4.2.3.tar.gz

# Start building cppzmq
cd cppzmq-4.2.3
mkdir build
cd build
cmake ..
doas make install
```

Build oscillate: `env DEVELOPER_LOCAL_TOOLS=1 BOOST_ROOT=/usr/local make release-static`

### On Solaris:

The default Solaris linker can't be used, you have to install GNU ld, then run cmake manually with the path to your copy of GNU ld:

        mkdir -p build/release
        cd build/release
        cmake -DCMAKE_LINKER=/path/to/ld -D CMAKE_BUILD_TYPE=Release ../..
        cd ../..

Then you can run make as usual.

### On Linux for Android (using docker):

        # Build image
        docker build -f utils/build_scripts/android32.Dockerfile -t oscillate-android .
        # Create container
        docker create -it --name oscillate-android oscillate-android bash
        # Get binaries
        docker cp oscillate-android:/opt/android/oscillate/build/release/bin .

### Building portable statically linked binaries

By default, in either dynamically or statically linked builds, binaries target the specific host processor on which the build happens and are not portable to other processors. Portable binaries can be built using the following targets:

* ```make release-static-linux-x86_64``` builds binaries on Linux on x86_64 portable across POSIX systems on x86_64 processors
* ```make release-static-linux-i686``` builds binaries on Linux on x86_64 or i686 portable across POSIX systems on i686 processors
* ```make release-static-linux-armv8``` builds binaries on Linux portable across POSIX systems on armv8 processors
* ```make release-static-linux-armv7``` builds binaries on Linux portable across POSIX systems on armv7 processors
* ```make release-static-linux-armv6``` builds binaries on Linux portable across POSIX systems on armv6 processors
* ```make release-static-win64``` builds binaries on 64-bit Windows portable across 64-bit Windows systems

### Cross Compiling

You can also cross-compile Oscillate static binaries on Linux for Windows and macOS with the `depends` system.

* ```make depends target=x86_64-linux-gnu``` for 64-bit linux binaries.
* ```make depends target=x86_64-w64-mingw32``` for 64-bit windows binaries. Requires: python3 g++-mingw-w64-x86-64 wine1.6 bc
* ```make depends target=x86_64-apple-darwin14``` for macOS binaries. Requires: cmake imagemagick libcap-dev librsvg2-bin libz-dev libbz2-dev libtiff-tools python3-dev curl libtiff-tools bsdmainutils libbz2-dev python3-setuptools
* ```make depends target=i686-linux-gnu``` for 32-bit linux binaries. Requires: g++-multilib bc
* ```make depends target=arm-linux-gnueabihf``` for armv7 binaries. Requires: g++-arm-linux-gnueabihf
* ```make depends target=aarch64-linux-gnu``` for armv8 binaries. Requires: g++-aarch64-linux-gnu

*** For `x86_64-apple-darwin14` you need to download SDK first ***    

* ```git clone -b oscillate https://github.com/malbit/MacOSX-SDKs.git contrib/depends/SDKs ```    

You can download SDK at https://github.com/malbit/MacOSX-SDKs/releases/download/MacOSX10.11.sdk.oscillate/MacOSX10.11.sdk.tar.gz and unpack it and put to contrib/depends/SDKs    

The required packages are the names for each toolchain on apt. Depending on your OS Distribution, they may have different names.

Using `depends` might also be easier to compile Oscillate on Windows than using MSYS. Activate Windows Subsystem for Linux (WSL) with a distribution (for example Ubuntu), install the apt build-essentials and follow the `depends` steps as stated above.

### Compability with older Linux Versions < GLIBC_2.25

* ```make depends-compat target=x86_64-linux-gnu``` for 64-bit linux binaries.


## Running oscillated

The build places the binary in `bin/` sub-directory within the build directory
from which cmake was invoked (repository root by default). To run in
foreground:

    ./bin/oscillated

To list all available options, run `./bin/oscillated --help`.  Options can be
specified either on the command line or in a configuration file passed by the
`--config-file` argument.  To specify an option in the configuration file, add
a line with the syntax `argumentname=value`, where `argumentname` is the name
of the argument without the leading dashes, for example `log-level=1`.

To run in background:

    ./bin/oscillated --log-file oscillated.log --detach

To run as a systemd service, copy
[oscillated.service](utils/systemd/oscillated.service) to `/etc/systemd/system/` and
[oscillated.conf](utils/conf/oscillated.conf) to `/etc/`. The [example
service](utils/systemd/oscillated.service) assumes that the user `oscillate` exists
and its home is the data directory specified in the [example
config](utils/conf/oscillated.conf).

If you're on Mac, you may need to add the `--max-concurrency 1` option to
oscillate-wallet-cli, and possibly oscillated, if you get crashes refreshing.

## Internationalization

See [README.i18n.md](README.i18n.md).

## Using Tor

> There is a new, still experimental, [integration with Tor](ANONYMITY_NETWORKS.md). The
> feature allows connecting over IPv4 and Tor simultaneously - IPv4 is used for
> relaying blocks and relaying transactions received by peers whereas Tor is
> used solely for relaying transactions received over local RPC. This provides
> privacy and better protection against surrounding node (sybil) attacks.

While Oscillate isn't made to integrate with Tor, it can be used wrapped with torsocks, by
setting the following configuration parameters and environment variables:

* `--p2p-bind-ip 127.0.0.1` on the command line or `p2p-bind-ip=127.0.0.1` in
  oscillated.conf to disable listening for connections on external interfaces.
* `--no-igd` on the command line or `no-igd=1` in oscillated.conf to disable IGD
  (UPnP port forwarding negotiation), which is pointless with Tor.
* `DNS_PUBLIC=tcp` or `DNS_PUBLIC=tcp://x.x.x.x` where x.x.x.x is the IP of the
  desired DNS server, for DNS requests to go over TCP, so that they are routed
  through Tor. When IP is not specified, oscillated uses the default list of
  servers defined in [src/common/dns_utils.cpp](src/common/dns_utils.cpp).
* `TORSOCKS_ALLOW_INBOUND=1` to tell torsocks to allow oscillated to bind to interfaces
   to accept connections from the wallet. On some Linux systems, torsocks
   allows binding to localhost by default, so setting this variable is only
   necessary to allow binding to local LAN/VPN interfaces to allow wallets to
   connect from remote hosts. On other systems, it may be needed for local wallets
   as well.
* Do NOT pass `--detach` when running through torsocks with systemd, (see
  [utils/systemd/oscillated.service](utils/systemd/oscillated.service) for details).
* If you use the wallet with a Tor daemon via the loopback IP (eg, 127.0.0.1:9050),
  then use `--untrusted-daemon` unless it is your own hidden service.

Example command line to start oscillated through Tor:

    DNS_PUBLIC=tcp torsocks oscillated --p2p-bind-ip 127.0.0.1 --no-igd

### Using Tor on Tails

TAILS ships with a very restrictive set of firewall rules. Therefore, you need
to add a rule to allow this connection too, in addition to telling torsocks to
allow inbound connections. Full example:

    sudo iptables -I OUTPUT 2 -p tcp -d 127.0.0.1 -m tcp --dport 19994 -j ACCEPT
    DNS_PUBLIC=tcp torsocks ./oscillated --p2p-bind-ip 127.0.0.1 --no-igd --rpc-bind-ip 127.0.0.1 \
        --data-dir /home/amnesia/Persistent/your/directory/to/the/blockchain

## Debugging

This section contains general instructions for debugging failed installs or problems encountered with Oscillate. First ensure you are running the latest version built from the Github repository.

### Obtaining stack traces and core dumps on Unix systems

We generally use the tool `gdb` (GNU debugger) to provide stack trace functionality, and `ulimit` to provide core dumps in builds which crash or segfault.

* To use gdb in order to obtain a stack trace for a build that has stalled:

Run the build.

Once it stalls, enter the following command:

```
gdb /path/to/oscillated `pidof oscillated`
```

Type `thread apply all bt` within gdb in order to obtain the stack trace

* If however the core dumps or segfaults:

Enter `ulimit -c unlimited` on the command line to enable unlimited filesizes for core dumps

Enter `echo core | sudo tee /proc/sys/kernel/core_pattern` to stop cores from being hijacked by other tools

Run the build.

When it terminates with an output along the lines of "Segmentation fault (core dumped)", there should be a core dump file in the same directory as oscillated. It may be named just `core`, or `core.xxxx` with numbers appended.

You can now analyse this core dump with `gdb` as follows:

`gdb /path/to/oscillated /path/to/dumpfile`

Print the stack trace with `bt`

* To run oscillate within gdb:

Type `gdb /path/to/oscillated`

Pass command-line options with `--args` followed by the relevant arguments

Type `run` to run oscillated

### Analysing memory corruption

We use the tool `valgrind` for this.

Run with `valgrind /path/to/oscillated`. It will be slow.

### LMDB

Instructions for debugging suspected blockchain corruption as per @HYC

There is an `mdb_stat` command in the LMDB source that can print statistics about the database but it's not routinely built. This can be built with the following command:

`cd ~/oscillate/external/db_drivers/liblmdb && make`

The output of `mdb_stat -ea <path to blockchain dir>` will indicate inconsistencies in the blocks, block_heights and block_info table.

The output of `mdb_dump -s blocks <path to blockchain dir>` and `mdb_dump -s block_info <path to blockchain dir>` is useful for indicating whether blocks and block_info contain the same keys.

These records are dumped as hex data, where the first line is the key and the second line is the data.
