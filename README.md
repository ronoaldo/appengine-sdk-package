appengine-sdk-package
=====================

Simple tool to build .deb packages from binary AppEngine SDK releases.

Why?
====

Makes easier to deploy a new SDK release for Python/Go/PHP on multiple machines, 
so you can help your developers keep up-to-date with your SDK.

Can be used to Java, but the Maven releases cover that already.

Quick how to
============

* Only Go SDK supported at this time.

Install dependencies on your Debian-based linux box:

    # apt-get install devscripts build-essential cdbs dh-make

Build the .deb from source root

    $ git clone https://github.com/ronoaldo/appengine-sdk-package
    $ cd appengine-sdk-package && debuild
    $ cd ..

Install the package with dpkg (su / sudo):

    # dpkg -i appengine-sdk-package*.deb

Start building .deb from AppEngine SDK binary distributions:

    $ wget http://googleappengine.googlecode.com/files/go_appengine_sdk_linux_amd64-1.8.2.zip
    $ make-sdk-pkg go_appengine_sdk_linux_amd64-1.8.2.zip

Install the SDK deb system-wide:

    # dpkg -i go-appengine-sdk*.deb

Have fun!
