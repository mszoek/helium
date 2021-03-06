# What is Airyx?

Airyx is a new open source OS project that aims to provide a similar experience and some compatibiilty with macOS on x86-64 sytems. It builds on the solid foundations of FreeBSD, existing open source packages in the same space, and new code to fill the gaps. Please visit [airyx.org](https://airyx.org/) or join us on [Libera IRC](https://libera.chat) in `#airyx` for more info!

![](https://api.cirrus-ci.com/github/mszoek/airyx.svg?branch=main&task=airyx)

The main design goals are:
- source compatibility with macOS applications (i.e. you could compile a Mac application on Airyx and run it)
- similar GUI metaphors and familiar UX (file manager, application launcher, top menu bar that reflects the open application, etc)
- compatible with macOS filesystems (HFS+ and APFS) and folder layouts (/Library, /System, /Users, /Volumes, etc)
- self-contained applications in [folders](https://github.com/AppImage/AppImageKit/wiki/AppDir) or a [single file](https://github.com/AppImage) and a (mostly) installer-less experience for /Applications
- mostly maintain compatibility with the FreeBSD base system and X11 - a standard Unix environment under the hood
- compatible with Linux binaries via FreeBSD's Linux support
- eventual compatibility with x86-64 macOS binaries (Mach-O) and libraries
- pleasant to use, secure, stable, and performant


## Why BSD instead of Linux?

In theory, it will be easier to build Mac code on FreeBSD because it is closer to macOS than Linux is. BSD kernels also support a foreign system call interface which should help make emulating Mach system calls easier, and eliminates the need to emulate BSD system calls like [Darling](https://docs.darlinghq.org/internals/basics/system-call-emulation.html) (on Linux) does. Also, why not? Devils need love too!

## Is this... legally sketchy?

No. Consider projects like [ReactOS](https://reactos.org/faq/), a from-scratch effort to create an OS compatible with Microsoft Windows, [GNUstep](http://www,gnustep.org), which provides an open implementation of Cocoa APIs and other things, or [Darling](https://darlinghq.org), a Darwin (macOS) emulation on Linux. Airyx is similar and stands on the shoulders of many such projects.

All code used is freely available under open source licenses. No proprietary elements like fonts, icons, trademarks, etc can be used. Original code must be written using "clean room" techniques - that is, from public documentation like developer guides by people who have never seen the proprietary code - and released under the [FreeBSD license](https://opensource.org/licenses/BSD-2-Clause) or the [MIT license](https://opensource.org/licenses/MIT).

## What programming languages does Airyx use?

The goal is to use a small core set of languages as much as possible: the "C" family (C, C++, Objective-C), Swift, Python, Java, and shell scripts. This should cover most needs.

## I can code in those! How can I help?

Great! Take a look at the [issues](https://github.com/mszoek/airyx/issues) list to find something that interests you, or contact [mszoek](https://github.com/mszoek).

## I don't code. Can I still help?

Absolutely! There will be art, documentation, testing, UX and UI work, release management, project management, legal advice, and many other ways to contribute. Check out the [issues](https://github.com/mszoek/airyx/issues) for ideas on how to contribute, or contact [mszoek](https://github.com/mszoek).

One really big way to help right now would be a project logo! Got some art skills? Go nuts!

## This is a huge effort. Y'all must be crazy!

Probably. But...

!["Here's to the crazy ones. The misfits. The rebels. The troublemakers. The round pegs in the square holes. The ones who see things differently. They're not fond of rules. And they have no respect for the status quo. You can quote them, disagree with them, glorify or vilify them. About the only thing you can't do is ignore them. Because they change things. The push the human race forward. And while some may see them as the crazy ones, we see genius. Because the people who are crazy enough to think they can change the world, are the ones who do."](https://i.etsystatic.com/9865576/r/il/3afeb0/1019438891/il_794xN.1019438891_m9og.jpg)


## Acknowledgements
This project would not be possible without the generous support of [Cirrus CI](https://cirrus-ci.org/) for CI/CD and [Cloudsmith](https://cloudsmith.io/) for package hosting! Thanks to these awesome organizations for supporting open source software!

[![Packages hosted by: Cloudsmith](https://img.shields.io/badge/OSS%20hosting%20by-cloudsmith-blue?logo=cloudsmith&style=flat-square)](https://cloudsmith.com)
