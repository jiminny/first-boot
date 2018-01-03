FirstBoot
======

FirstBoot is a script to set up an macOS laptop for web and mobile development.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Requirements
------------

We support:

* macOS High Sierra (10.13)

Older versions may work but aren't regularly tested.

Install
-------

Download the script:

```sh
curl --remote-name https://raw.githubusercontent.com/jiminny/first-boot/master/mac
```

Review the script (avoid running scripts you haven't read!):

```sh
less mac
```

Execute the downloaded script:

```sh
sh mac 2>&1 | tee ~/first-boot.log
```

Optionally, review the log:

```sh
less ~/first-boot.log
```

Debugging
---------

Your last Laptop run will be saved to `~/first-boot.log`.
Read through it to see if you can debug the issue yourself.
If not, copy the lines where the script failed into a
[new GitHub Issue](https://github.com/jiminny/first-boot/issues/new).
Or, attach the whole log file as an attachment.

What it sets up
---------------

macOS tools:

* [Homebrew] for managing operating system libraries.

[Homebrew]: http://brew.sh/

Programming languages, package managers, and configuration:

* [NPM] for installing JavaScript packages
* [Ruby] stable for writing general-purpose code
* [Yarn] for managing JavaScript packages

[NPM]: https://www.npmjs.org/
[Yarn]: https://yarnpkg.com/en/


It should take less than 15 minutes to install (depends on your machine).
