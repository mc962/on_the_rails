---
layout: post
title:  "Getting Started With Ruby!"
date:   2022-06-01 23:45:40 -0400
categories: ruby setup
---
If you're reading this, you've already decided that Ruby is the next language for you. As with many languages, there tends to be a few ways to get things set up correctly on your system.

## System Dependencies
Ruby may need certain dependencies to build and run properly (such as OpenSSL for example). Some of these may coincidentally be installed when you set up other programs, or even your Ruby version manager. Here is a list of some common packages that are less likely to be already installed when trying to install Ruby on a new system.
### Linux
I am using Ubuntu as the example Operating System here. Other Operating Systems such as Fedora may use a slightly different ecosystem, with similar but slightly differently-named packages.

In the case of Ubuntu, packages may be installed individually, or all together with a command like `sudo apt update && sudo apt install packageA packageB packageC`

- git
- build-essential - contains a variety of common "essential" build tools and packages that may be required by other tools and packages
- curl
- libssl-dev - necessary for compiling Ruby's openssl extension
- zlib1g-dev - necessary for compiling Ruby's zlib extension

### MacOS
- Xcode - MacOS is a bit unique in that a lot of basic developer tools are recommended to be installed first through Xcode. Installing this will take care of many initial libraries such as Git.
### Windows
Follow whatever your installer for Ruby on Windows asks if using the Installer option.

## Version Managers

### Unix

#### rbenv
A version manager for managing and switching between Ruby versions. I've found this one to be the easiest to install and set up, while listing the latest Ruby versions.
**Link:** https://github.com/rbenv/rbenv

#### rvm
Another version manager for managing and switching between Ruby versions. It has a lot more features than simpler managers like `rbenv`, and is maybe slightly easier for someone without much Ruby ecosystem knowledge to install. However, I've rarely had much use personally for these extra features. Furthermore, at least historically, `rvm` would stick files and configuration all over the system and not always successfully uninstall them if one wants to switch. Therefore, I personally do not recommend `rvm` very much anymore. 
**Link:** https://rvm.io/rvm

#### System
Many package managers that come with your Operating System (Linux apt,yum, Apple Homebrew, etc.) often have a version of Ruby that may be installed through them. This is generally the easiest way to install Ruby. However, the version offered is often out of date, and so I often recommend using what is offered from a version manager as listed above.

### Windows
For a long time setting up and running Ruby and Ruby projects was considered painful on Windows. Personally, at least for basic stuff, I have found that Ruby has come a long way on Windows, and may be installed fairly easily using the supplied installers.
**Link:** https://rubyinstaller.org/

If running a Linux version on Windows using Windows Subsystem for Linux, you may also install Ruby using the version managers listed in [Unix](#unix), as this is essentially the same process as installing on any Linux OS.


NOTE: Only install and run at most **_1_** Ruby version manager at a time. If you run more than one, they will likely conflict in ways that are hard to understand and prevent you from working with Ruby properly.


Finally, when in doubt, go to the source on Ruby's [homepage](https://www.ruby-lang.org/en/documentation/installation/). The instructions there are quite good as well.