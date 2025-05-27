[skonfig](https://skonfig.li) is a system configuration and automation framework
designed to work with all systems, from your toaster to the data centre.
All you need is an SSH connection and a POSIX/UNIX-like shell environment.

And best of all: you already know how to use it (if you know shell scripts).

skonfig uses three main repositories:

* [skonfig](https://github.com/skonfig/skonfig) - implementation of the **skonfig** executable,
* [base](https://github.com/skonfig/base) - explorer and types for **general use**,
* [extra](https://github.com/skonfig/extra) - **special purpose** types and incubator for new types.

Check out the [skonfig](https://github.com/skonfig/skonfig) repository to learn
how to get started.

**Need support?** You can find us in `#skonfig:matrix.org` ([matrix?](https://matrix.org/faq/)).

## What are *base* and *extra*?

**base** explorers and types are used to change the state of the operating
system or core components of it and are not for some specific piece of
software. Furthermore, the quality requirements for inclusion in base are
higher than for extra.

**extra** contains types for specific purposes like configuring software or
services which don't belong to the operating system and also serves as an
incubator for new types.

Even more types can be found in sets specialised in helping you configure a
specific piece of software. Some of these sets can be found in this organization.

And being a fork of [cdist](https://cdi.st/) originally, your cdist manifests
and types will continue to work with skonfig with no or minimal adjustments.
