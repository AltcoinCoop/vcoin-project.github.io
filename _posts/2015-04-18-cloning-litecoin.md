---
layout: post
title: Cloning Litecoin
modified:
excerpt: Step-by-step instructions for cloning Litecoin (0.8.*)
author: graham_higgins
date: 2015-04-18T00:57:10+01:00
tags: [altcoin, cloning]
---

# Cloning Litecoin

1. Pre Installers.
    - 1a. Winrar
    - 1b. Compression
    - 1c. MinGW
2. Windows Deps.
    - 2a. OpenSSL
    - 2b.Berkeley DB
    - 2c. Boost
    - 2d. MiniUPNP
    - 2e. Protoc and Libprotobuf
    - 2f. Libpng
    - 2g. qrencode
3. Download and Compile QT.
4. The Clone
    - 4a. Source Code
    - 4b. Copy and Replace Litecoin
    - 4c. Copy and Replace LTC
    - 4d. Change rpc and port numbers. 
    - 4e. Change starting letter for addresses.
    - 4f. Update client version number.
    - 4g. Change Litecoin example addresses to Clonecoin Addresses. 
    - 4h. Change char pchMessageStart and ParseHex. 
    - 4i. Change alert keys. 
    - 4j. Remove Merkel root and Genesis Block.
    - 4k. Remove Nonce and testnet genesis. 
    - 4l. Add Epoochtime and Timestamp.
    - 4m. Fixing the checkpoints.
    - 4n. Change max money supply and coinbase maturity.
    - 4o. Change block times from 2.5 minutes to 30 seconds.
    - 4p. Change re-targeting
    - 4q. Add premine and change block rewards. 
    - 4r. Update Images.
    - 4s. Update Seed node/ AWS Seed node guide.
5. Hashing the Genesis Block and Merkel Root.
    - 5a. Ability to hash Genesis Block.
    - 5b. Compiling Clonecoin Windows QT.
    - 5c. Generating Merkel Root
    - 5d. Hashing the Genesis Block.
6. Connecting your nodes.
    - 6a. Create a conf.
    - 6b. Connect- server and home network.
7. Checkpointing the premine.
8. Clean up Your Code.
9. Compiling Clonecoind.
    - 9a. Compile Clonecoind.
    - 9b. Remove and cleanup.
10. Github for release, made easy.
    - 10a. Easy Pushing Commits/Launch code.
    - 10b. Easy Revert Commits
    - 10c. Easy Pushing Updates.
11. Common Errors
12. Quick Logos
13. The Website.
    - 13a. The Template.
    - 13b. Upload to a website.
14. The Launch. Ninja vs Pumped vs ICO.
    - 14a. Prelaunch
    - 14b. The Ninja
    - 14c. The Pumped.
    - 14d. The ICO.


## 1. Pre Installers.

### 1a. File Compressor/Extractor

Download and install Winrar or an alternate file compression tool. 
[http://www.rarlab.com/download.htm](http://www.rarlab.com/download.htm)

### 1b. Text Editor.

Download and install a text editor such as [Sublime Text](http://www.sublimetext.com/). You need a text editor that can easily search and replace case sensitive text.

### 1c. Download and install MingW

[http://sourceforge.net/projects/mingw/files/Installer/mingw-get-setup.exe/download](http://sourceforge.net/projects/mingw/files/Installer/mingw-get-setup.exe/download)

Double click to install, keep the checkbox for the GUI checked and make sure to install in ``C:\MinGW``. Press continue. From the MinGW GUI interface, go to ``all packages -> MYSYS``
Right click on the following installations and mark for installation.

- ``msys-base-bin`` (may highlight other checkboxes which is fine)
- ``msys-autoconf-bin``
- ``msys-automake-bin``
- ``msys-libtool-bin``

Click on ``Installation -> Apply changes``. MinGW will now download the remaining packages. Make sure to remove any previous installs of MinGW before starting. 

Once complete, navigate to ``C:\MinGW\bin`` and you should only have a ``mingw-get`` application. If you have ``msys-gcc`` and ``msys-w32api`` you need to delete MinGW and check the correct install packages are selected above.

Download and extract mingw32 to ``C:\mingw32``, [http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/4.9.1/theads-posix/dwarf/i686-4.9.1-release-posix-dwarf-rt_v3-rev1.7z/download](http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/4.9.1/theads-posix/dwarf/i686-4.9.1-release-posix-dwarf-rt_v3-rev1.7z/download)

You now need to change the path variables. Go to ``control panel->system`` and ``security->system``. Click on ``advanced system properties->environmental variables``. In the top box navigate to PATH and change to 

    > C:\mingw32\bin;%SystemRoot%\system32;%SystemRoot%;%SystemRoot%\System32\Wbem;%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\


Checking your MingW install.

To start the MingW app navigate to ``C:\MinGW\msys\1.0\msys.bat``, create a desktop shortcut as you will use the ``msys`` command as well as the windows command prompts. Double click to start and enter the following to display the version and correct paths.

    $ gcc -v

Your ``msys`` output should look like the following code.

    $ gcc -v
    Using built-in specs.
    COLLECT_GCC=c:\mingw32\bin\gcc.exe
    COLLECT_LTO_WRAPPER=c:/mingw32/bin/../libexec/gcc/i686-w64-mingw32/4.9.1/lto-wrapper.exe
    Target: i686-w64-mingw32
    Configured with: ../../../src/gcc-4.9.1/configure --host=i686-w64-mingw32 --build=i686-w64-mingw32 --target=i686-w64-mingw32 --prefix=/
    mingw32 --with-sysroot=/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32 --with-gxx-include-dir=/mingw32/i686-w64-mingw32/include/c++
     --enable-shared --enable-static --disable-multilib --enable-languages=ada,c,c++,fortran,objc,obj-c++,lto --enable-libstdcxx-time=yes -
    -enable-threads=posix --enable-libgomp --enable-libatomic --enable-lto --enable-graphite --enable-checking=release --enable-fully-dynam
    ic-string --enable-version-specific-runtime-libs --disable-sjlj-exceptions --with-dwarf2 --disable-isl-version-check --disable-cloog-ve
    rsion-check --disable-libstdcxx-pch --disable-libstdcxx-debug --enable-bootstrap --disable-rpath --disable-win32-registry --disable-nls
     --disable-werror --disable-symvers --with-gnu-as --with-gnu-ld --with-arch=i686 --with-tune=generic --with-libiconv --with-system-zlib
     --with-gmp=/c/mingw491/prerequisites/i686-w64-mingw32-static --with-mpfr=/c/mingw491/prerequisites/i686-w64-mingw32-static --with-mpc=
    /c/mingw491/prerequisites/i686-w64-mingw32-static --with-isl=/c/mingw491/prerequisites/i686-w64-mingw32-static --with-cloog=/c/mingw491
    /prerequisites/i686-w64-mingw32-static --enable-cloog-backend=isl --with-pkgversion='i686-posix-dwarf-rev1, Built by MinGW-W64 project'
     --with-bugurl=http://sourceforge.net/projects/mingw-w64 CFLAGS='-O2 -pipe -I/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32/opt/in
    clude -I/c/mingw491/prerequisites/i686-zlib-static/include -I/c/mingw491/prerequisites/i686-w64-mingw32-static/include' CXXFLAGS='-O2 -
    pipe -I/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32/opt/include -I/c/mingw491/prerequisites/i686-zlib-static/include -I/c/mingw4
    91/prerequisites/i686-w64-mingw32-static/include' CPPFLAGS= LDFLAGS='-pipe -L/c/mingw491/i686-491-posix-dwarf-rt_v3-rev1/mingw32/opt/li
    b -L/c/mingw491/prerequisites/i686-zlib-static/lib -L/c/mingw491/prerequisites/i686-w64-mingw32-static/lib -Wl,--large-address-aware'
    Thread model: posix
    gcc version 4.9.1 (i686-posix-dwarf-rev1, Built by MinGW-W64 project)

If you are having issues I have uploaded a MinGW install [here](https://howtocloneanaltcoin.com/downloads/MinGW.rar)
 
## 2. Download and Install Dependencies.

Create a deps folder at ``C:\deps``.  If you want to cheat you can download the pre-built dependencies [here](http://www.mediafire.com/download/y89546s65sf8de5/deps.zip), though it is recommended to build your own.

### 2a. OpenSLL

Install OpenSSL dependencies on Windows.

Download the latest version of OpenSSL [https://www.openssl.org/source/openssl-1.0.1j.tar.gz](https://www.openssl.org/source/openssl-1.0.1j.tar.gz) to your deps folder.

Open the MinGW shell at ``C:\MinGW\msys\1.0\msys.bat`` 

    $ cd /c/deps/
    $ tar xvfz openssl-1.0.1j.tar.gz
    $ cd openssl-1.0.1j
    $ ./Configure no-zlib no-shared no-dso no-krb5 no-camellia no-capieng no-cast no-cms no-dtls1 no-gost no-gmp no-heartbeats no-idea no-jpake no-md2 no-mdc2 no-rc5 no-rdrand no-rfc3779 no-rsax no-sctp no-seed no-sha0 no-static_engine no-whirlpool no-rc2 no-rc4 no-ssl2 no-ssl3 mingw
    $ make


### 2b. Berkeley DB

Download [http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz](http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz) and place in your deps folder.

In the MinGW shell use the following code.

    $ cd /c/deps/
    $ tar xvfz db-4.8.30.NC.tar.gz
    $ cd db-4.8.30.NC/build_unix
    $ ../dist/configure --enable-mingw --enable-cxx --disable-shared --disable-replication
    $ make


### 2c. Boost

Download Boost to your deps folder. [http://sourceforge.net/projects/boost/files/boost/1.55.0/boost_1_55_0.zip/download](http://sourceforge.net/projects/boost/files/boost/1.55.0/boost_1_55_0.zip/download)
 
Make sure to download either the 7z or zip versions. Double click on the folder to extract ``boost_1_55_0`` in your deps folder. This may take several minutes depending on your PC's speed. 

Using the Windows command prompt, bootstrap and compile boost. To bring up the windows command prompt just type ``cmd`` in the windows search bar.


    > cd C:\deps\boost_1_55_0\
    > bootstrap.bat mingw
    > b2 --build-type=complete --with-chrono --with-filesystem --with-program_options --with-system --with-thread toolset=gcc variant=release link=static threading=multi runtime-link=static stage


### 2d. Mini UPNP

Download and extract MiniUPNP [http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.9.20140911.tar.gz](http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.9.20140911.tar.gz) to your deps folder. 

Rename  folder from ``miniupnpc-1.9.20140911`` to ``miniupnpc`` then from a Windows command prompt:

    $ cd C:\deps\miniupnpc
    $ mingw32-make -f Makefile.mingw init upnpc-static


### 2e. Protoc and Libprotobuf:

Download and extract [http://protobuf.googlecode.com/files/protobuf-2.5.0.zip](http://protobuf.googlecode.com/files/protobuf-2.5.0.zip) to your deps folder.

In the ``msys`` shell run

    $ cd /c/deps/protobuf-2.5.0
    $ configure --disable-shared
    $ make


### 2f. libpng

Download and extract [http://prdownloads.sourceforge.net/libpng/libpng-1.6.14.tar.gz?download](http://prdownloads.sourceforge.net/libpng/libpng-1.6.14.tar.gz?download) to your deps folder. Extract.

In ``msys`` shell run 

    $ cd /c/deps/libpng-1.6.14
    $ configure --disable-shared
    $ make
    $ cp .libs/libpng16.a .libs/libpng.a


### 2g. qrencode

Download and extract [http://fukuchi.org/works/qrencode/qrencode-3.4.4.tar.gz](http://fukuchi.org/works/qrencode/qrencode-3.4.4.tar.gz) to your deps folder.

In ``msys`` shell run 

    $ cd /c/deps/qrencode-3.4.4

    $ LIBS="../libpng-1.6.14/.libs/libpng.a ../../mingw32/i686-w64-mingw32/lib/libz.a" \
    png_CFLAGS="-I../libpng-1.6.14" \
    png_LIBS="-L../libpng-1.6.14/.libs" \
    configure --enable-static --disable-shared --without-tools

    $ make

## 3. Download and Compile QT.

Download and uncompress [http://download.qt-project.org/official_releases/qt/4.8/4.8.6/qt-everywhere-opensource-src-4.8.6.zip](http://download.qt-project.org/official_releases/qt/4.8/4.8.6/qt-everywhere-opensource-src-4.8.6.zip) to ``C:\Qt\4.8.6``.

 Once again check it resides in ``C:\Qt\4.8.6`` not ``C:\Qt\4.8.6\4.8.6``. Due to a bug in 4.8.6 you will need to apply the patch available [here](https://codereview.qt-project.org/#/c/84567/3/tools/configure/configureapp.cpp).

 For those who can't find or work it out, you need to change the following lines in ``C:\Qt\4.8.6\tools\configure\configureapp.cpp`` or download the patched file [here](https://www.mediafire.com/?y4urdzfp0k0j0gm)
 and replace it in C:\Qt\4.8.6\tools\configure\configureapp.cpp


    2180  |  -  const QString mingwPath = dictionary["QMAKESPEC"].endsWith("-g++") ?
    2180  |  +  const QString mingwPath = dictionary["QMAKESPEC"].contains("-g++") ?
    2252  |  -  if (dictionary["QMAKESPEC"].endsWith("-g++")+
    2252  |  +  if (dictionary["QMAKESPEC"].contains("-g++")+


From your Windows command prompt run 

    $ cd C:\Qt\4.8.6
    $ configure -release -opensource -confirm-license -static -no-sql-sqlite -no-qt3support -no-opengl -qt-zlib -no-gif -qt-libpng -qt-libmng -no-libtiff -qt-libjpeg -no-dsp -no-vcproj -no-openssl -no-dbus -no-phonon -no-phonon-backend -no-multimedia -no-audio-backend -no-webkit -no-script -no-scripttools -no-declarative -no-declarative-debug -qt-style-windows -qt-style-windowsxp -qt-style-windowsvista -no-style-plastique -no-style-cleanlooks -no-style-motif -no-style-cde -nomake demos -nomake examples
    $ mingw32-make


Now we are ready to start the cloning process.

If you are worried about compilation, it would be wise to jump ahead and ensure everything is working with compiling the client  before working with the clone.

## 4. The Clone

In this guide we will be cloning Litecoin. Litecoin is a Scrypt based coin and the original altcoin. I will be calling this coin “Clonecoin” (CLN).

### 4a. Download and extract the Litecoin source.
 
[https://github.com/litecoin-project/litecoin](https://github.com/litecoin-project/litecoin)

In this guide I will be placing the source code in ``C:\Clonecoin``

### 4b. Copy and Replace Litecoin 

Using your test editor, search out and replace all instances of “Litecoin” with “Clonecoin”. Make sure your search is case sensitive and search for all instances, replace “Litecoin” with “Clonecoin”, “litecoin” with “clonecoin” etc. Run a search without case sensitivity before continuing to ensure you have all instances.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/61a9b7b8ea5db179b30f979d109847e473d0de81](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/61a9b7b8ea5db179b30f979d109847e473d0de81)


### 4c. Copy and Replace LTC.
 
Using your test editor, search out and replace all instances of “LTC” with “CLN”.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7b6a2ad68deb97caab802c460ebfe5104fa72e2c](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7b6a2ad68deb97caab802c460ebfe5104fa72e2c)


### 4d. Change rpc and port numbers.

Search for an appropriate port and rpc number [http://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers](http://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers).

Litecoin uses  port 9333 testnet 19333, rpcport 9332 testnet 19332. We will change them to port 10333 testnet 11333, rpcport 10332 testnet 11332

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7f149b069f77b3e174ca8a7b10b98287c3e663a9](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/7f149b069f77b3e174ca8a7b10b98287c3e663a9)


### 4e. Change starting letter for addresses.
 
In this case we change the 48 to 28, therefore all addresses will start with “C”.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d0621b86a358e93495658d564640144458aab8ee](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d0621b86a358e93495658d564640144458aab8ee)


### 4f. Update client version number. 

Since its really a fork of Litecoin we will bring the version numbers up to 1.0.0.0.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/95d0bef6e6a7bf27f3ed6d8153fccf8275524ba9](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/95d0bef6e6a7bf27f3ed6d8153fccf8275524ba9)


### 4g. Change Litecoin example addresses to Clonecoin Addresses. 

Here we change the LTC addresss ``Ler4HNAEfwYhBmGXcFP2Po1NpRUEiK8km2`` to a Clonecoin mystery address starting with c. (see step 6d)

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/9a5321bfb9b0482ed3b435edb815d8eee268b949](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/9a5321bfb9b0482ed3b435edb815d8eee268b949)


### 4h. Change char pchMessageStart and ParseHex.
 
We want these to be unique to Clonecoin. Be wary of changing ``pchMessageStart`` to to letters other than ``a-f``. All numbers are fine to use.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/011b9a8e713821d8010a827f7aeacf09c772a267](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/011b9a8e713821d8010a827f7aeacf09c772a267)


### 4i. Change alert keys
. 
We just change these to be different from Litecoin to avoid the Litecoin messages.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/0798f246007c9196bcfcf39c2ef2222a660d59d2](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/0798f246007c9196bcfcf39c2ef2222a660d59d2)


### 4j. Remove Merkel root and Genesis Block.

These will be replaced later on. Though for now and in the near future they are no longer needed.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/46bbcb1377ac2db0f8dabc19faffb9ab6f989cb6](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/46bbcb1377ac2db0f8dabc19faffb9ab6f989cb6)

### 4k. Remove Nonce and testnet genesis. 

We remove the testnet genesis block and nonce.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/24cf6793c02369fc60a8b67645818f0cf7d1252a](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/24cf6793c02369fc60a8b67645818f0cf7d1252a)

### 4l. Add Epochtime and Timestamp.
 
To create a genesis block we need an epoch time and a verbal timestamp. The current epoch time can be obtained from [http://www.epochconverter.com/](http://www.epochconverter.com/) and the latest news headline can be used for the verbal timestamp. We also replace the testnet timestamp.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/790f9964abdb0543abe1ee1801562a004349e719](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/790f9964abdb0543abe1ee1801562a004349e719)


### 4m. Fixing the checkpoints.
 
We comment out the hardcoded checkpoint and change the genesis block checkpoint.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/fe0d86a278f4d6470bee697a25256b0340cfc9fd](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/fe0d86a278f4d6470bee697a25256b0340cfc9fd)


### 4n. Change max money supply and coinbase maturity.
 
We just multiplied total coins by 10 and reduced coin based maturity. The higher the number of confirmations the better for the network.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c43361429062f04b5697f9e9fca19e2f15d2e634](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c43361429062f04b5697f9e9fca19e2f15d2e634)


### 4o. Change block times from 2.5 minutes to 30 seconds.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8796946bd1d3d5d15d06ba0e72e4b6bbf1fe1d06](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8796946bd1d3d5d15d06ba0e72e4b6bbf1fe1d06)


### 4p. Change re-targeting from the ridiculous 2.5 days to every 5 minutes.
 
This is cutting out a small portion of instamining. 

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/a3df6e9dc15009bdb22c60a496c109334cc55864](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/a3df6e9dc15009bdb22c60a496c109334cc55864)


### 4q. Add premine and change block rewards.
 
Since we initially increased block rewards by x10, we will increase the base reward from 50 to 500. We then add a premine on block 2 as well as a staggered decrease in block sizes.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/ddc36732b46fbc38ca06012be127ff994177192d](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/ddc36732b46fbc38ca06012be127ff994177192d)


### 4r. Update Images.

If you have not already, you will need a splash and logo.
You will need to update ``src/rec/icons`` - ``bitcoin.png``, ``bitcoin_testnet.png``, ``bitcoin.icon``, ``bitcoin_testnet.icon`` (all 256x256 pixels), ``toolbar.png`` and ``toolbar_testnet.png`` (16x16 pixels).

Also update ``src/res/images``, ``splash.png``, ``splash_testnet.png`` and ``about.png``.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/08edb2f2648acc373e60c44fbd0558c514697ff7](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/08edb2f2648acc373e60c44fbd0558c514697ff7)


### 4s. Update Seed node- 

First you will need to create a dedicated node. This is a quick easy guide.

Head to [Amazon AWS console](https://console.aws.amazon.com) and create an account. Click on the EC2 link on the left. See [AWS pricing](http://aws.amazon.com/ec2/pricing/)

Create and instance, select ``Microsoft Windows Server 2012 R2 Base``, select your server preference - we chose ``t2.micro`` which is free tier eligible.

Click ``Next: Configure Instance Details``, highlight ``Protect against accidental termination``, click review and launch.

Go to security settings, open all ports and click launch. Create a security key pair and make sure to download it and keep it safe. Launch your instance.

On the aws instance home screen click the Elastic IP tab, click ``allocate Ip address`` and confirm. While still in the Elastic IP tab, click ``allocate`` and allocate to the instance by clicking the top checkbox and identifying your server. Confirm. Your instance will take around 15 minutes to launch.

To connect. Click the instance tab, highlight your instance and press ``connect``. Using your key from earlier, you are now able to download a server shortcut and server password.

Using your new Elastic IP, replace your new IP removing Litecoin old seed nodes. 

``src/net.cpp``

    static const char *strMainNetDNSSeed[][2] = {
       {"clonecointools.com", "54.232.218.200"},
       {NULL, NULL}
    };

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/92e520e8a80294a1964bca707ddca704c2c0bdc9](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/92e520e8a80294a1964bca707ddca704c2c0bdc9)


### 4.t Change the name of the ``bitcoin-qt.pro`` file to ``clonecoin-qt.pro``

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d309822b3b6519ca6424ac74df054ad351db1d88](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d309822b3b6519ca6424ac74df054ad351db1d88)



## 5. Hashing the Genesis Block and Merkel Root. 

### 5a. Ability to hash Genesis Block.

We now need to add the ability to hash a new genesis block so we add the following code to main.cpp.

``main.cpp``

    if (true && block.GetHash() != hashGenesisBlock)
    {
        printf("Searching for genesis block...\n");
        // This will figure out a valid hash and Nonce if you're
        // creating a different genesis block:
        uint256 hashTarget = CBigNum().SetCompact(block.nBits).getuint256();
        uint256 thash;
        char scratchpad[SCRYPT_SCRATCHPAD_SIZE];

        loop
        {
            scrypt_1024_1_1_256_sp(BEGIN(block.nVersion), BEGIN(thash), scratchpad);
            if (thash <= hashTarget)
                break;
            if ((block.nNonce & 0xFFF) == 0)
            {
                printf("nonce %08X: hash = %s (target = %s)\n", block.nNonce, thash.ToString().c_str(), hashTarget.ToString().c_str());
            }
            ++block.nNonce;
            if (block.nNonce == 0)
            {
                printf("NONCE WRAPPED, incrementing time\n");
                ++block.nTime;
            }
        }
        printf("block.nTime = %u \n", block.nTime);
        printf("block.nNonce = %u \n", block.nNonce);
        printf("block.GetHash = %s\n", block.GetHash().ToString().c_str());
      
    }

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8b2e543c6f9c6dde0ebb8a7b73fd06c6d7de18ec](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/8b2e543c6f9c6dde0ebb8a7b73fd06c6d7de18ec)


### 5b. Compiling Clonecoin Windows QT.

Create ``libleveldb.a`` and ``libmemenv.a``. 

Using Msys shell, run. For this we have Clonecoin in ``C:/Clonecoin``

    $ cd /C/clonecoin/src/leveldb
    $ TARGET_OS=NATIVE_WINDOWS make libleveldb.a libmemenv.a

If the file already exists, Msys will inform you so.

Open your ``Clonecoin-qt.pro`` file.

We now need to change the dependency directory locations 

    # Dependency library locations can be customized with:
    #   BOOST_INCLUDE_PATH, BOOST_LIB_PATH, BDB_INCLUDE_PATH,
    #   BDB_LIB_PATH, OPENSSL_INCLUDE_PATH and OPENSSL_LIB_PATH respectively

    OBJECTS_DIR = build
    MOC_DIR = build
    UI_DIR = build


to


    # Dependency library locations can be customized with:
    #   BOOST_INCLUDE_PATH, BOOST_LIB_PATH, BDB_INCLUDE_PATH,
    #   BDB_LIB_PATH, OPENSSL_INCLUDE_PATH and OPENSSL_LIB_PATH respectively
    BOOST_LIB_SUFFIX=-mgw49-mt-s-1_55
    BOOST_INCLUDE_PATH=C:/deps/boost_1_55_0
    BOOST_LIB_PATH=C:/deps/boost_1_55_0/stage/lib
    BDB_INCLUDE_PATH=C:/deps/db-4.8.30.NC/build_unix
    BDB_LIB_PATH=C:/deps/db-4.8.30.NC/build_unix
    OPENSSL_INCLUDE_PATH=C:/deps/openssl-1.0.1j/include
    OPENSSL_LIB_PATH=C:/deps/openssl-1.0.1j
    MINIUPNPC_INCLUDE_PATH=C:/deps/
    MINIUPNPC_LIB_PATH=C:/deps/miniupnpc
    QRENCODE_INCLUDE_PATH=C:/deps/qrencode-3.4.4
    QRENCODE_LIB_PATH=C:/deps/qrencode-3.4.4/.libs
    OBJECTS_DIR = build
    MOC_DIR = build
    UI_DIR = build


and comment out the ``genleveldb`` command


    genleveldb.commands = cd $$PWD/src/leveldb && CC=$$QMAKE_CC CXX=$$QMAKE_CXX $(MAKE) OPT=\"$$QMAKE_CXXFLAGS 


to


    #genleveldb.commands = cd $$PWD/src/leveldb && CC=$$QMAKE_CC CXX=$$QMAKE_CXX $(MAKE) OPT=\"$$QMAKE_CXXFLAGS 


and add the flags for a static build.

Add


    CONFIG += static


to 


    CONFIG += thread
    CONFIG += static


and 
 

    win32:QMAKE_LFLAGS *= -Wl,--large-address-aware


to


    win32:QMAKE_LFLAGS *= -Wl,--large-address-aware  -static


Now from the Windows cmd, run  


    > set PATH=%PATH%;C:\Qt\4.8.6\bin
    > cd C:\clonecoin\
    > qmake "USE_QRCODE=1" "USE_UPNP=1" "USE_IPV6=1" clonecoin-qt.pro
    > mingw32-make -f Makefile.Release

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/5c82150b6d017412f6df4f06f86941de2bebae83](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/5c82150b6d017412f6df4f06f86941de2bebae83)


Your ``Clonecoin-qt`` should now be available in your ``C:\clonecoin\release`` folder after around 5 minutes. If errors occur, scroll up and read them try to identify and fix.

### 5c. Generating Merkel Root

Start your ``Clonecoin-qt``. You should see an error Assertion failed! 

Navigate to your Clonecoin appdata folder ``C:\Users\(YOUR*PC*NAME)\AppData\Roaming\Clonecoin`` and open the debug log in a text editor. The folder is hidden by default, so typing ``%appdata%`` in the Windows search bar will bring up access to the roaming\clonecoin folder.

Scroll to the bottom of the text to find the following lines.

    2014-11-06 17:00:04 LoadBlockIndexDB(): last block file = 0
    2014-11-06 17:00:04 LoadBlockIndexDB(): transaction index disabled
    2014-11-06 17:00:04 Initializing databases...
    2014-11-06 17:00:04 71154501f2bb79422cb9d06775463810e8ae59243460250f6c942ebd3a9712dd
    2014-11-06 17:00:04 0000000000000000000000000000000000000000000000000000000000000000
    2014-11-06 17:00:04 d010ddcc6651af0e28e50ee36096e438b7974da9d58f1be95a968b180756a0c8


The bottom hash is the merkel root, we take this and add it to ``main.cpp``

    assert(block.hashMerkleRoot == uint256("0xd010ddcc6651af0e28e50ee36096e438b7974da9d58f1be95a968b180756a0c8"));

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c776fb6da5599cc9a3bde9749880d9a1f9a1222a](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/c776fb6da5599cc9a3bde9749880d9a1f9a1222a)


### 5d. Hashing the Genesis Block.

We now need to recompile the client in Windows ``cmd``. You can remove the path and directory if you still have the client open.

    > set PATH=%PATH%;C:\Qt\4.8.6\bin
    > cd C:\clonecoin\
    > qmake "USE_QRCODE=1" "USE_UPNP=1" "USE_IPV6=1" clonecoin-qt.pro
    > mingw32-make -f Makefile.Release


Restart the client. The previous Merkel error should  not occur and the client should appear to hang on launch. It is now hashing your genesis block.

How long this takes can vary from a few seconds to minutes. Once the client hangs with a genesis block error, open your debug text file again in your Clonecoin appdata folder ``C:\Users\(YOUR*PC*NAME)\AppData\Roaming\Clonecoin``

    2014-11-05 18:29:11 block.nNonce = 2110551 
    2014-11-05 18:29:11 block.GetHash = 235b6e7fa788b4a0914a959c7ccb38f6cb2706a4c5bd68c0d64f22ba7772baf9

We will now add these to ``main.ccp``.

    @@ -35,7 +35,7 @@ CTxMemPool mempool;
    unsigned int nTransactionsUpdated = 0;

    map<uint256, CBlockIndex*> mapBlockIndex;
    uint256 hashGenesisBlock("0x");
    uint256 hashGenesisBlock("0x235b6e7fa788b4a0914a959c7ccb38f6cb2706a4c5bd68c0d64f22ba7772baf9");
    static CBigNum bnProofOfWorkLimit(~uint256(0) >> 20); // Clonecoin: starting difficulty is 1 / 2^12
    CBlockIndex* pindexGenesisBlock = NULL;
    int nBestHeight = -1;
    @@ -2757,7 +2757,7 @@ bool LoadBlockIndex()
         pchMessageStart[1] = 0xb2;
         pchMessageStart[2] = 0xa4;
         pchMessageStart[3] = 0xdc;
         hashGenesisBlock = uint256("0x");
         hashGenesisBlock = uint256("0x235b6e7fa788b4a0914a959c7ccb38f6cb2706a4c5bd68c0d64f22ba7772baf9");
       }

       //
    @@ -2804,12 +2804,12 @@ bool InitBlockIndex() {
         block.nVersion = 1;
         block.nTime   = 1415210670;
         block.nBits   = 0x1e0ffff0;
         block.nNonce  = 0;
         block.nNonce  = 2110551;

         if (fTestNet)
         {
           block.nTime   = 1415210670;
           block.nNonce  = 0;
           block.nNonce  = 2110551;
         }

         //// debug print

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/789abc8f316efe9026a781c28934e3d3df69f57a](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/789abc8f316efe9026a781c28934e3d3df69f57a)


Recompile the Windows QT. From the Windows ``cmd``, run  

    > set PATH=%PATH%;C:\Qt\4.8.6\bin
    > cd C:\clonecoin\
    > qmake "USE_QRCODE=1" "USE_UPNP=1" "USE_IPV6=1" clonecoin-qt.pro
    > mingw32-make -f Makefile.Release


Your ``Clonecoin-qt`` should now be available in your ``C:\clonecoin\release`` folder.

## 6. Connecting your nodes.

Now you have your client we need to connect the nodes to check everything is working. You can use testnet though its just as easy to use mainnet. 

Connect to your server we set up earlier or use another local machine.

### 6a. Create a conf. file.

We only create this now to enable mining to check the network.

Your conf. file should be placed in ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin``.

To create a conf file, right click ``new->text document``. Copy and paste the code below replacing a suitable username and password. Click ``save``, change file type to ``all`` and save as ``clonecoin.conf``. Or just [download this one](https://www.mediafire.com/?taozsy80yaay1bz)


    rpcuser=Yourusername
    rpcpassword=Yourpassword
    rpcallowip=127.0.0.1
    daemon=1
    server=1
    listen=1
    port=10333
    rpcport=10332
    addnode=54.232.218.200


### 6b. Connect

#### Server

Upload your client to the server and start the client. The two clients should connect. 

#### Home Network

You may need to add your local IPs to the conf file. To do this type ``cmd`` to bring up command prompt, type ``ipconfig`` and use the IPv4 address in your ``addnode`` settings on both machines.


    rpcuser=Yourusername
    rpcpassword=Yourpassword
    rpcallowip=127.0.0.1
    daemon=1
    server=1
    listen=1
    port=10333
    rpcport=10332
    addnode=10.0.0.18
    addnode=10.0.0.31


Once both clients are connected you can start to mine blocks.

You can either use the traditional Scrypt miner or type ``setgenerate true -1`` into your main console.

Mine as many blocks as you want, checking diff adjustment and ensure block rewards are correct. It is advised to confirm some transactions, send some coins and check the client for any errors or adjustments.

In this case I missed the toolbar.png and testnet_toolbar.png as a deliberate example of why you "SHOULD ALWAYS CHECK YOUR CLIENT BEFORE RELEASE"

If you want to restart the chain you need to delete the chain by going to your Clonecoin roaming folder on both machines and deleting everything. 

## 7. Checkpointing the premine.

If you followed all the steps above you should be sitting with a lovely source code and compiled client.

We have a few things to finish and checkpointing the premine is highly important.

Many coin launches have been lost by people not knowing or forgetting to do this step. Without a checkpoint you can very likely kiss your premine goodbye to a hash attack on launch.

Start your compiled clients on both machines. Since we deleted the blockchain earlier mine your premine, plus 2-3 blocks.

Open the concole on the clonecoin client and type; ``getblockhash 1``, ``getblockhash 2``, ``getblockhash 3``. We will use these three hashes to checkpoint the premine.

We also need some data from the ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin\debug`` file. 

We are looking for the details of the highest checkpointed block, in this case block 3. 

    2014-11-11 15:02:57 SetBestChain: new best=718732cb3323ceaa46c8fc5fd521e7f7e31e424c59cc2a02e4e39c2c7306a649  height=3 log2_work=22.000022 tx=4 date=2014-11-11 15:02:57 progress=1.000000

You will need to convert the last block time to an epochtime date i.e. in this instance, from 2014-11-11 15:02:57 to 1415718177. [Use epochconverter for convenience](http://www.epochconverter.com/)

Now we add the block hashes for blocks 1, 2 and 3 and insert the highest block (block 3) details into the  checkpoint block details. We also add the estimated number of transactions per day after the checkpoint.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d5e61c1d0e7678cc165acf9dc1a27c6d23200030.](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/d5e61c1d0e7678cc165acf9dc1a27c6d23200030.)


Recompile your client.

Back up your  ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin`` folder. This now has your premine. 

You now need to check the checkpoints are correct. On the client that does not have the premine, navigate to ``C:\Users\(YOUR**PC**NAME)\AppData\Roaming\clonecoin`` and delete everything EXCEPT ``wallet.dat`` (very important, DO NOT DELETE) and ``clonecoin.conf`` files.

Restart the client. If your checkpoints are correct the client should update and sync without issues. 


## 8. Clean up your code.

Clean up your ``README`` with your new specifications, rewards, website etc.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/13fc52d07ed55d5b95071a043e88b13a6ad92a67](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/13fc52d07ed55d5b95071a043e88b13a6ad92a67)


Remove your build deps and changes from ``clonecoin-qt.pro``

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/437d50f106d588edd95fd35eec06b2da7cf3d49e](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/437d50f106d588edd95fd35eec06b2da7cf3d49e)



## 9. Compiling Clonecoind.

### 9a. Compile Clonecoind

Navigate to  ``C:\clonecoin\src\makefile.mingw`` and open with your text editor. You will see:


    USE_UPNP:=-
    USE_IPV6:=1

    DEPSDIR?=/usr/local
    BOOST_SUFFIX?=-mgw46-mt-sd-1_52

    INCLUDEPATHS= \
     -I"$(CURDIR)" \
     -I"$(DEPSDIR)/include"

    LIBPATHS= \
     -L"$(CURDIR)/leveldb" \
     -L"$(DEPSDIR)/lib"

    LIBS= \
     -l leveldb \
     -l memenv \
     -l boost_system$(BOOST_SUFFIX) \
     -l boost_filesystem$(BOOST_SUFFIX) \
     -l boost_program_options$(BOOST_SUFFIX) \
     -l boost_thread$(BOOST_SUFFIX) \
     -l boost_chrono$(BOOST_SUFFIX) \
     -l db_cxx \
     -l ssl \
     -l crypto

    DEFS=-D_MT -DWIN32 -D_WINDOWS -DBOOST_THREAD_USE_LIB -DBOOST_SPIRIT_THREADSAFE
    DEBUGFLAGS=-g
    CFLAGS=-mthreads -O2 -w -Wall -Wextra -Wformat -Wformat-security -Wno-unused-parameter $(DEBUGFLAGS) $(DEFS) $(INCLUDEPATHS)
    # enable: ASLR, DEP and large address aware
    LDFLAGS=-Wl,--dynamicbase -Wl,--nxcompat -Wl,--large-address-aware


change it to read:


    USE_UPNP:=1
    USE_IPV6:=1

    DEPSDIR?=/usr/local
    BOOST_SUFFIX?=-mgw49-mt-s-1_55

    INCLUDEPATHS= \
     -I"$(CURDIR)" \
     -I"/c/deps/boost_1_55_0" \
     -I"/c/deps" \
     -I"/c/deps/db-4.8.30.NC/build_unix" \
     -I"/c/deps/openssl-1.0.1j/include"
     
    LIBPATHS= \
     -L"$(CURDIR)/leveldb" \
     -L"/c/deps/boost_1_55_0/stage/lib" \
     -L"/c/deps/miniupnpc" \
     -L"/c/deps/db-4.8.30.NC/build_unix" \
     -L"/c/deps/openssl-1.0.1j"

    LIBS= \
     -l leveldb \
     -l memenv \
     -l boost_system$(BOOST_SUFFIX) \
     -l boost_filesystem$(BOOST_SUFFIX) \
     -l boost_program_options$(BOOST_SUFFIX) \
     -l boost_thread$(BOOST_SUFFIX) \
     -l boost_chrono$(BOOST_SUFFIX) \
     -l db_cxx \
     -l ssl \
     -l crypto

    DEFS=-D_MT -DWIN32 -D_WINDOWS -DBOOST_THREAD_USE_LIB -DBOOST_SPIRIT_THREADSAFE
    DEBUGFLAGS=-g
    CFLAGS=-mthreads -O2 -w -Wall -Wextra -Wformat -Wformat-security -Wno-unused-parameter $(DEBUGFLAGS) $(DEFS) $(INCLUDEPATHS)
    # enable: ASLR, DEP and large address aware
    LDFLAGS=-Wl,--dynamicbase -Wl,--nxcompat -Wl,--large-address-aware -static


We change the deps to point to the deps we created earlier. If you chose to place your deps in a different folder, change the code to point to your folders. We also used ``-static`` in ``LDFLAGS=-Wl,--dynamicbase -Wl,--nxcompat -Wl,--large-address-aware -static`` for a static linked exe,  updated UPNP Includes and Lib paths to enable UPNP.

In the Msys shell, you can now compile litecoind.

    cd /c/clonecoin/src
    make -f makefile.mingw
    strip clonecoind.exe


Your clonecoind should now be in your C:\clonecoin\src folder.

###### [https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/6b124d98f059fb42b2b8837b520b6a626ec6f5ef](https://github.com/HowToCloneAnAltcoin/Clonecoin/commit/6b124d98f059fb42b2b8837b520b6a626ec6f5ef)


### 9b. Remove libleveldb.a and libmemev.a from C:\Clonecoin\src\leveldb.

Remove your ``Clonecoin-qt`` from the release folder and zip for release. 

Delete the release, debug and build folders. This is your code for release.


## 10. Github for release, made easy.

1. Create a Github account.
2. Download the [latest Github Windows client](https://windows.github.com/). Then run the Github install and use your login details from Github to log into the client.
3. Navigate to you Github account, click ``repositories->new``. Enter the repository name, description and public or private. “Public” allows everyone to see your code and is recommended for advanced users who can push codes quickly. Most launches will choose a paid private account, allowing them to pre-load the release source code and open the repository from public to private instantly. Click done, then on the next screen click the green “Set up in Desktop” button. Allow the browser to launch the Github client, select the location of your Github depositories, usually in the Github folder of your documents. Click “OK”. You now have a folder that you can update your source code and easily push commits to Github.

### 10a. Easy Pushing Commits/Launch Code.

Copy and paste your source code into the ``documents/github/yourcoinnamefolder``. In your Windows Github client, click on your client name on the left hand side.

Your Github client should recognise a host of changes if present. Fill in the commit details, select the files that need to be committed, usually all and on by default and press commit. 

On the top right hand side will be a publish or sync box, click that and the Github Windows client will push the changes and source code to your repository on Github.

### 10b. Easy Revert Commits.

Open your Github client and ensure it's sync'd. Highlight your repository. Click on the commit to you wish to rollback, then revert.

On the top right hand side will be a publish or sync box, click that and the Github Windows client will push the revert to your repository on Github.

### 10c. Easy Pushing Updates.

Log into your Github Windows client. Click on the altcoin tab in the left and click sync to ensure your local code is up to date.

Edit your local code in your ``documents/github/yourcoinname`` folder.

Once your Github client picks up the changes enter the commit details and commit to Github.

## 11. Common Errors/Mistakes.

### I am getting "this" error.

Most errors can be solved with a little effort. The compiler will usually display an error message or warning. Read it.

If it's UPNP error check your directories in your pro file, then check your UPNP deps, rebuild them.

Google it. Most things can be solved far quicker with a little investigation into the errors vs posting in a forum and awaiting reply.

### I am still seeing the old logos on my desktop shortcuts.

Windows cache has cached the image. The easiest way to solve this is run a program such as Glarys Utilities to clear your PC. Also delete the build folder in between builds to ensure your builds are clean.

### Makefile.Release:291: recipe for target 'release\clonecoin-qt.exe' failed

Close your client.


## 12. Creating your own logo.

There are a few easy ways to get a logo. If you have Photoshop and want a easy template try [http://apsdfile.com/coin-generator-for-photoshop/](http://apsdfile.com/coin-generator-for-photoshop/).

Install GIMP. GIMP is a free utility available to download from [http://www.gimp.org/](http://www.gimp.org/) and try youtube vids. 

For those looking for an even faster alternative try tools like [http://www.onlinebadgemaker.com/3d-badge-maker](http://www.onlinebadgemaker.com/3d-badge-maker).

These can be used for quick launches or temporary images while you wait, purchase or make an official one.

## 13. The Website.

### 13a. The Template.

Download and install a free website editor, [Bluegriffon](http://bluegriffon.org/) is a prime example.

Find yourself a [suitable template](http://www.freshdesignweb.com/free-html5-css3-templates.html). Download and edit the template with all your coin details. 

### 13b. Upload to a website.

Create an account at [Namecheap](http://www.namecheap.com/), they accept BTC.

Register the domain and commission hosting at the same time, that way there is no DNS delay.

Usually you can pick up a year hosting with domain and SSL if you want for under .15 BTC.

If this is a one-off coin launch then a simple hosting plan will suffice. If you're looking to launch more coins, choose a dedicated server or reseller plan.

Once your order is confirmed log into cpanel with the details provided, enable cloudflare and ssl of you purchased it.

Single hosting plans will require support for SSL, dedicated or reseller accounts have the ability to self enable through WHM.

In CPanel, go to file manager and upload your site to the public_html folder. Your website should be now viewable on your domain.


## 14. The Launch. Ninja vs Pumped vs ICO.

Launching a coin is the make or break point. The style of launch will dictate how to prepare.

### 14a. Prelaunch.

The key to a good launch is timing and consistency. Don't release the code early and make sure it works.

Create your Bitcointalk account. The earlier the better to get rid of posting restrictions on new accounts.

Create accounts on Twitter, Facebook, cryptocointalk, IRC, Reddit and all the usual channels.

### 14b. The Ninja

This gives the developer more time, no restrictions with no one looking or ready. With these coins you can set the network up early and don't have people looking for the code.

Uploading the code to github a minute easily will likely be enough time to stop anyone searching. Website can go live early and some argue it gives miners a better chance.

Usually a ninja launch involves a instamine allowing the developers to mine many blocks.

### 14c. The Pumped.

Harder to do. The pre-hype means you will have people looking for the code on Github and websites.

Your code needs to be solid to handle a massive intake of hashing power and be prepared for the harshest critics.

### 14d. The ICO.

An advanced pump coin that needs a reliable escrow, good hype and delivery of goods.

Most ICO's deliver nothing but BTC to the developer and broken promises to the users.

Find a good escrow, take time with your code and remember to keep an open and clear communication.

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>
