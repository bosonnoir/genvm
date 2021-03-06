![GenVM](http://www.genvm.eu/img/logo.png "GenVM")

GenVM Is a poerfull script designed to generate minimum and complete 
Debian and Ubuntu virtual machines for KVM/QEMU (so usable in ProxMox, 
libvirtd, ...), VirtualBox and VMWare.

GenVM is distributed under GPL3.

Sources are avalable from GitHub (http://github.com/genvm) and 
documentation is available on http://www.genvm.eu.

# Tested distributions

GenVM was tested on Debian Wheezy, Jessie and Stretch, Ubuntu Trusty and
Arch Linux.

# Generated VM

| Distrib. | Name    | Rev    | Cool  |
| -------- |:-------:|:------:|:-----:|
| debian   | wheezy  |  7.X   | i386  |
| debian   | wheezy  |  7.X   | amd64 |
| debian   | jessie  |  8.X   | i386  |
| debian   | jessie  |  8.X   | amd64 |
| debian   | stretch |  9.X   | i386  |
| debian   | stretch |  9.X   | amd64 |
| ubuntu   | precise |  12.04 | i386  |
| ubuntu   | precise |  12.04 | amd64 |
| ubuntu   | trusty  |  14.04 | i386  |
| ubuntu   | trusty  |  14.04 | amd64 |
| ubuntu   | vivid   |  15.04 | i386  |
| ubuntu   | vivid   |  15.04 | amd64 |
| ubuntu   | wily    |  15.10 | i386  |
| ubuntu   | wily    |  15.10 | amd64 |
 
# Installation

No special installation needed, only download the last version of GenVM,
adjust permissions and launch it via sudo or su.

## from sources

    $ git clone https://github.com/genvm/genvm.git
    Cloning into 'genvm'...
    remote: Counting objects: 125, done.
    remote: Compressing objects: 100% (45/45), done.
    remote: Total 125 (delta 39), reused 123 (delta 39), pack-reused 0
    Receiving objects: 100% (125/125), 44.15 KiB | 0 bytes/s, done.
    Resolving deltas: 100% (39/39), done.
    Checking connectivity... done.
    $ cd genvm
    $ ls
    genvm

## from archive

### Last version (dev)

    $ wget -q https://github.com/genvm/genvm/archive/master.zip
    $ unzip master.zip
    Archive:  master.zip
    1d5aa137931b15e6307a0fedb0c30f118c79a959
      creating: genvm-master/
      inflating: genvm-master/genvm      

### Stable version

You can find stables version from GitHub on page :
https://github.com/genvm/genvm/tags

Download the last version and extract it like last version.

# Examples

Consult http://www.genvm.eu for all documentations.

## Simple Debian

    $ su -c "./genvm debian-stable.vmdk"
    Password:
    Set password to root > 
    Enter new UNIX password: 
    Retype new UNIX password: 
    passwd: password updated successfully
    $ ls -lh debian-stable.vmdk
    -rw-r--r-- 1 root users 875M Jul 27 17:33 debian-stable.vmdk

## Simple Ubuntu

    $ su -c "genvm -b grub-pc -k linux-image-generic \
     -n trusty \
     -S http://archive.ubuntu.com/ubuntu/ \
     -V trusty ubuntu-trusty.vmdk"

# Contact

team at genvm dot eu
