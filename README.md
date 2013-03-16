Getting Started
---------------

To get started with PAC-man, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the PAC-man trees, use a command like this:

    repo init -u git://github.com/PAC-man/android.git -b cm-10.1

To sync up:

    repo sync

Then to build:

    ./build-pac.sh <device_name>
    example: ./build-pac.sh urushi

You need help while compiling for your Device?
You get them in our official IRC Channel:

[IRC Channel: #pac-rom](http://webchat.freenode.net/?channels=pac-rom)
