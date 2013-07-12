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


Submitting Patches
------------------
We're open source, and patches are always welcome!
You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -a
    git push ssh://<username>@review.pac-rom.com:29418/<project> HEAD:refs/for/cm-10.1

Register at review.pac-rom.com and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't repo start again), but instead of git commit -a
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [PAC-man Code Review](http://review.pac-rom.com/)


Getting Started
---------------

To get started with PAC-man, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the PAC-man trees, use a command like this:

    repo init -u git://github.com/PAC-man/android.git -b <branch>

Then to sync up:

    repo sync

Then to build:

    ./build-pac.sh <device_name>

For information on how to build, check [Here](http://forum.xda-developers.com/showthread.php?t=2060017)
Our Official IRC Channel: [#pac-rom](http://webchat.freenode.net/?channels=pac-rom)
