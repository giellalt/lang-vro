 The Võro morphology and tools / Võro keeleoppus ja -tüüriistaq
================================================================

[![GitHub issues](https://img.shields.io/github/issues-raw/giellalt/lang-vro)](https://github.com/giellalt/lang-vro/issues)
[![Build Status](https://github.com/giellalt/lang-vro/workflows/Speller%20CI+CD/badge.svg)](https://github.com/giellalt/lang-vro/actions)
[![License](https://img.shields.io/github/license/giellalt/lang-vro)](https://raw.githubusercontent.com/giellalt/lang-vro/main/LICENSE)

This directory contains source files for the Võro language morphology
and dictionary. The data and implementation are licenced under __LICENCE__
licence, also detailed in the
[LICENSE](https://github.com/giellalt/lang-vro/blob/main/LICENSE). The
authors named in the AUTHORS file are available to grant other licencing choices.

Install proofing tools and [keyboards](https://github.com/giellalt/keyboard-vro)
for the Võro language by using the [Divvun Installer](http://divvun.no)
(some languages are only available via the nightly channel).

Documentation can be found here:

- [In source documentation generated with github
   pages](https://gilellalt.github.io/lang-vro/)
- https://giellalt.uit.no/lang/vro/VoroDocumentation.html (analyser)
- https://giellalt.uit.no/index.html (infrastructure)

Core dependencies
-----------------

In order to compile and use __UNDEFINED__ language morphology and
dictionaries, you need:

- an FST compiler: [HFST](https://github.com/hfst/hfst), [Foma](https://github.com/mhulden/foma) or [Xerox Xfst](https://web.stanford.edu/~laurik/fsmbook/home.html)
- [VislCG3](https://visl.sdu.dk/svn/visl/tools/vislcg3/trunk) Constraint Grammar tools

To install VislCG3 and HFST, just copy/paste this into your Terminal on **Mac OS X**:

```
curl https://apertium.projectjj.com/osx/install-nightly.sh | sudo bash
```

or terminal on **Ubuntu, Debian or Windows Subsystem for Linux**:

```
wget https://apertium.projectjj.com/apt/install-nightly.sh -O - | sudo bash
sudo apt-get install cg3 hfst
```

or terminal on **RedHat, Fedora, CentOS or Windows Subsystem for Linux**:

```
wget https://apertium.projectjj.com/rpm/install-nightly.sh -O - | sudo bash
sudo dnf install cg3 hfst
```

Alternatively, the Apertium wiki has good instructions on how to [install the dependencies for Mac
OS X](https://wiki.apertium.org/wiki/Apertium_on_Mac_OS_X) and how to [install
the dependencies on
linux](https://wiki.apertium.org/wiki/Installation_of_grammar_libraries)

Further details and dependencies are described on the GiellaLT [Getting Started](https://giellalt.uit.no/infra/GettingStarted.html) pages.

Downloading
-----------

Using Git:
```
git clone https://github.com/giellalt/lang-vro
```

Using Subversion:
```
svn checkout https://github.com/giellalt/lang-vro.git/trunk lang-vro
```

Building and installation
-------------------------

[INSTALL](https://github.com/giellalt/lang-vro/blob/main/INSTALL)
describes the GNU build system in detail, but for most users it is the usual:

```sh
./autogen.sh # This will automatically clone or check out other GiellaLT dependencies
./configure
make
(as root) make install
```
