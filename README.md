# openOCD: build from sources on multiple platforms

Each directory contains a Vagrantfile that compiles a static version of openOCD, ready to be deployed on the relevant architecture.

## prerequisites

- [https://www.virtualbox.org/wiki/Downloads](VirtualBox)
- [https://www.vagrantup.com/downloads.html](Vagrant)
- Vagrant plugin vagrant-vbguest (install with ``vagrant plugin install vagrant-vbguest``)
- internet connectivity

## usage

`` 
cd x86_64-pc-linux-gnu
vagrant up
vagrant halt
cd ..
cd i686-pc-linux-gnu
vagrant up
vagrant halt
cd ..
cd i686-mingw32
vagrant up
vagrant halt
cd ..
``

Vagrant will download and install everything for you; after compilation, you will find the archives

``
x86_64-pc-linux-gnu/openocd-0.10.0-static-x86_64-linux-gnu.tar.bz2
i686-pc-linux-gnu/openocd-0.10.0-static-i686-linux-gnu.tar.bz2
i686-mingw32/openocd-0.10.0-static-i686-mingw32.tar.bz2
``

ready to be deployed.
