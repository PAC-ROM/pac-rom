PAC-man - The AIO ROM
=====================

Support Our Sites
------------------------
We have created many different ways to follow us. Please visit and support our efforts

[PAC-man Website] (http://pac-rom.com)

[PAC-man Forum] (http://forum.pac-rom.com)

[PAC-man Downloads] (http://pacman.basketbuild.com)

[PAC-man Gerrit] (http://review.pac-rom.com)

[PAC-man Stats] (http://pac-rom.com/#Stats)

[PAC-man Google+] (https://plus.google.com/102557242936341392082/posts)

[PAC-man Facebook] (https://www.facebook.com/PACmanROMS)

[PAC-man Jenkins] (https://jenkins.pac-rom.com)


Submitting Patches
------------------
We're open source, and patches are always welcome!
You can send patches by using these commands:

    sudo apt-get install git-review
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
    git push ssh://<username>@review.pac-rom.com:29418/<project> HEAD:refs/for/pac-4.4


Register at [PAC-man Gerrit] (http://review.pac-rom.com) and use the username that you registered under with git-review. Make sure to add your ssh keys to your Gerrit profile

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

The git-review package will only have to be installed once

If you are going to make extra additions, just repeat steps (Don't repo start again), but instead of git commit -m
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [PAC-man Code Review](http://review.pac-rom.com/)


Getting Started
---------------

The first thing to do is prepare your machine to build, [use this guide for that!](https://github.com/PAC-man/android_vendor_pac/blob/pac-4.4/PrepareForBuild.md) if your machine is already configured to build, skip this step

After preparing your machine, continue with the following instructions:

To initialize your local repository using the PAC-man trees, use a command like this:

    repo init -u git://github.com/PAC-man/pacman.git -b <branch>

To initialize for KitKat on Linux

    repo init -u git://github.com/PAC-man/pacman.git -b pac-4.4 -g all,-notdefault,-darwin

To initialize for KitKat on MacOS

    repo init -u git://github.com/PAC-man/pacman.git -b pac-4.4 -g all,-notdefault,-linux

Then to sync up:

    repo sync -j#

Where # is the specific number of Jobs, 4 is default, change in accordance to internet performance/bandwidth/speed. Default is 4.

Then to build:

    ./build-pac.sh <device_code_name>

Example for Nexus 5:

    ./build-pac.sh hammerhead

For a list of supported commands run the script on it's own:

    ./build-pac.sh

To build with flags, this is the layout needed:
    ./build-pac.sh <Optional_flags> <device codename>

For an o3 optimization and Dex optimisations -if you don't understand, best to leave it- for the nexus 5 run:

    ./build-pac.sh -o3 -d hammerhead

You can also add a -j# before device_code_name for a selected number of jobs, usually No. of cores + 1 or 2


Device isn't supported? Not a problem, see [Adding Support] (https://github.com/PAC-man/android_vendor_pac/blob/pac-4.4/README.md) for how to add device support!

For information on how to build a general ROM from source, check [Here](http://forum.xda-developers.com/showthread.php?t=2649812)
