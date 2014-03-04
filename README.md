PAC-man - The AIO ROM
=====================

Support Our Sites
------------------------
We have created many different ways to follow us. Please visit and support our efforts

[PAC-man Website] (http://pac-rom.com/index.html)

[PAC-man Forum] (http://forum.pac-rom.com/)

[PAC-man Downloads] (http://pacman.basketbuild.com/index.php?dir=main/)

[PAC-man Gerrit] (http://review.pac-rom.com/)

[PAC-man Stats] (http://stats.pac-rom.com/stats)

[PAC-man Google+] (https://plus.google.com/102557242936341392082/posts)

[PAC-man Facebook] (https://www.facebook.com/PacManTheAioRom)


Submitting Patches
------------------
We're open source, and patches are always welcome!
You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -m "Message"
    git push ssh://<username>@review.pac-rom.com:29418/<project> HEAD:refs/for/pac-4.4


OR you can use our script to push, have a look at [pac-review] (http://pac-rom.com/downloads/pac-review)

Register at review.pac-rom.com and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't repo start again), but instead of git commit -m
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [PAC-man Code Review](http://review.pac-rom.com/)


Getting Started
---------------

To get started with PAC-man, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Setup build environment - http://forum.xda-developers.com/showthread.php?t=2224142

To initialize your local repository using the PAC-man trees, use a command like this:

    repo init -u git://github.com/PAC-man/pacman.git -b <branch>

To initialize for KitKat

    repo init -u git://github.com/PAC-man/pacman.git -b pac-4.4

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


Device isn't supported? Not a problem, see [Here] (http://forum.xda-developers.com/showthread.php?t=2662325) for how to build for an unsupported device!
For information on how to build a general ROM from source, check [Here](http://forum.xda-developers.com/showthread.php?t=2649812)
| Our Official IRC Channel: [#pac-rom](http://webchat.freenode.net/?channels=pac-rom)
