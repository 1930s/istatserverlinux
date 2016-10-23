# istatserver

istatserver is a system monitoring daemon that is used in conjunction with [iStat for iOS](https://bjango.com/ios/istat/) and [iStat for macOS](https://bjango.com/mac/istat/) to remotely monitor computers.

-----

### Supported OSs
- Linux
- FreeBSD, DragonFly BSD, OpenBSD, NetBSD and other BSD based OSs
- AIX
- Solaris
- HP-UX (Still in development and not tested)

-----

### Requirements
- C and C++ compilers such as gcc and g++.
- Auto tools (autoconf and automake).
- OpenSSL/libssl + development libraries.
- Sqlite3 + development libraries.
- libxml2 + development libraries.

We have a package guide [available](https://bjango.com/help/istat3/linuxpackages/) to help you install all the required packages for your OS.

-----

### Build procedure
- [Download](https://download.bjango.com/istatserverlinux.tar.gz) and decompress source
- cd /path/to/istatserver
- ./autogen
- ./configure
- make
- sudo make install
- sudo /usr/local/bin/istatserver -d (daemon mode)


A default passcode is generated on install. It can be found in the preference file, which is generally located at **/usr/local/etc/istatserver/istatserver.conf**. iStat for iOS and iStat for macOS will ask for this passcode the first time you connect to your computer.

-----

istatserver is based on [istatd](https://github.com/tiwilliam/istatd) by William Tisäter
