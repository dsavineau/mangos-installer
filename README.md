# MaNGOS Installer -- README

## Informations

mangos-installer is a shell script to unify MaNGOS installation on GNU/Linux distribution.

    $ ./mangos-installer
    Usage: ./mangos-installer: [OPTIONS]
          -p <path>       : Path to MaNGOS (default: /opt/mangos-<version>)
          -d              : Set in debug mode
          -j <number>     : Number of jobs for make (default 1)
          -v <version>    : Set MaNGOS version (classic|tbc|wotlk|cata)
          -h              : Print this help

This script does all steps to install MaNGOS according GNU/Linux distribution :

* Install all dependencies (git, openssl, cmake, etc...)
* Download MaNGOS and ScriptDev2
* Configure and Build

Sample output :

    $ ./mangos-installer -v classic -j 4
    -- GNU/Linux Debian
    -- Codename : jessie
    -- Release  : 8.6
    -- Package  : deb
    -- Platform : x86_64
    Installing dep... [OK]
    Cloning MaNGOS... [OK]
    Configuration...  [OK]
    Compiling...      [OK]
    Installing...     [OK]
    MaNGOS 0.18 (classic) has been installed !

All actions are logged in mangos-installer.log.

## Distributions

mangos-installer has been tested on several GNU/Linux distributions :

* Debian
 * Debian Lenny (5.0.x)
 * Debian Squeeze (6.0.x)
 * Debian Wheezy (7.x)
 * Debian Jessie (8.x)
* Ubuntu
 * Ubuntu Precise (12.04)
 * Ubuntu Quantal (12.10)
 * Ubuntu Raring (13.04)
 * Ubuntu Saucy (13.10)
 * Ubuntu Trusty (14.04)
 * Ubuntu Utopic (14.10)
 * Ubuntu Vivid (15.04)
* Centos
 * CentOS 5.x
 * CentOS 6.x
* Fedora
 * Fedora Lovelock (15)
 * Fedora Verne (16)
 * Fedora Beefy Miracle (17)
 * Fedora Spherical Cow (18)

## Architecture

mangos-installer has been tested on several architectures :

* x86 (32 bits)
* x86_64 (64 bits)

## Issues

* Debian Lenny (5.0.x) : You need to backport cmake (and libarchive also) from Squeeze because version is < 2.8
* Debian Lenny (5.0.x) : Don't use ACE packages from official repository because version is old
* CentOS 5.x : You need to install cmake >= 2.8 from rpm.pbone.net, pkgs.repoforge.org, etc...

## License

  This program is free software; you can redistribute it and/or modify
  it under the terms of the GNU General Public License as published by
  the Free Software Foundation; either version 2 of the License, or
  (at your option) any later version.

  This program is distributed in the hope that it will be useful,
  but WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  GNU General Public License for more details.

  You should have received a copy of the GNU General Public License
  along with this program.  If not, see <http://www.gnu.org/licenses/>.

  You can find the full license text in the file [COPYING](COPYING) delivered with this package.
