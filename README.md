PAC-ROM - The AIO ROM!
======================


Support Our Sites
=================

We have created many different ways to follow us. Please visit and support our efforts.

[PAC-ROM Website] (http://www.pac-rom.com/)

[PAC-ROM Forum] (http://forum.pac-rom.com/)

[PAC-ROM Downloads] (http://pacman.basketbuild.com/)

[PAC-ROM Gerrit] (http://review.pac-rom.com/)

[PAC-ROM GitHub] (http://review.pac-rom.com/)

[PAC-ROM Stats] (http://pac-rom.com/#Stats)

[PAC-ROM Google+] (https://plus.google.com/102557242936341392082/posts/)

[PAC-ROM Twitter] (https://twitter.com/pacroms/)

[PAC-ROM Facebook] (https://www.facebook.com/PACmanROMS/)

[PAC-ROM Jenkins] (https://jenkins.pac-rom.com/)


Instructions for sending to Gerrit
==================================

We're open source, and patches are always welcome!

Register at [Gerrit Code Review] (http://review.pac-rom.com/) and use the username that you registered with when using git-review. Make sure to add your ssh keys to your Gerrit profile. You must accept the [Contributors Agreement] (http://review.pac-rom.com/#/settings/agreements/) before submitting to Gerrit.

You can send patches by using these commands:

    sudo apt-get install git-review
    git clone https://github.com/PAC-man/<project>
    cd <project>
    <make edits>
    git add -A
    git commit -m "Message"
    git-review

OR you can use the convential method:

    cd <project>
    <make edits>
    git add -A
    git commit -m "Message"
    git push ssh://<username>@review.pac-rom.com:29418/<project> HEAD:refs/for/pac-5.0


The git-review package will only have to be installed once.

If you are going to make additional edits, just repeat steps, but instead of using:

    git commit -m "Message"

use:

    git commit --amend

Gerrit will recognize it as a new patch-set.

To view the status of your and others' patches, visit [Gerrit Code Review] (http://review.pac-rom.com/).


Getting Started
===============

The first thing to do is prepare your machine to build, [Use this guide for that!] (https://github.com/PAC-man/android_vendor_pac/blob/pac-5.0/PrepareForBuild.md) if your machine is already configured to build, skip this step.

After preparing your machine, continue with the following instructions:

To initialize your local repository using the PAC-ROM trees, use a command like this:

    repo init -u git://github.com/PAC-man/pacman.git -b <branch>

To initialize for Lollipop on Linux:

    repo init -u git://github.com/PAC-man/pacman.git -b pac-5.0 -g all,-notdefault,-darwin

To initialize for Lollipop on MacOS:

    repo init -u git://github.com/PAC-man/pacman.git -b pac-5.0 -g all,-notdefault,-linux

Then to sync up:

    repo sync -j#

Where # is the specific number of jobs, 4 is default, change in accordance to internet performance/bandwidth/speed. Default is 4.

Then to build:

    ./build-pac.sh <device_codename>

Example for Nexus 5:

    ./build-pac.sh hammerhead

For a list of supported commands run the script on it's own:

    ./build-pac.sh

To build with flags, this is the layout needed:
    ./build-pac.sh <optional_flags> <device_codename>

You can also add a -j# before device_codename for a selected number of jobs, usually number of cores + 1 or 2.


Device isn't supported? Not a problem, see [Adding Support] (https://github.com/PAC-man/android_vendor_pac/blob/pac-5.0/README.md) for how to add device support!

For information on how to build a general ROM from source, check [Here] (http://forum.xda-developers.com/showthread.php?t=2649812).
