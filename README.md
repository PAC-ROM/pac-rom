PAC-man - The AIO ROM
=====================

Submitting Patches
------------------
We're open source, and patches are always welcome!
You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -a
    git push ssh://<username>@code.nwwn.com:29418/<project> HEAD:refs/for/cm-10.1

Register at review.pac-man-rom.de and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't repo start again), but instead of git commit -a
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [PAC-man Code Review](http://review.pac-man-rom.de/)


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
Our Official Forum : [Forum](http://pac-man-rom.de/)
Our Official IRC Channel: [#pac-rom](http://webchat.freenode.net/?channels=pac-rom)