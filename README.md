# MaNGOS Installer -- README

## Information

mangos-installer is a shell script to unify MaNGOS installation on GNU/Linux distributions.

    $ ./mangos-installer
    Usage: ./mangos-installer: [OPTIONS]
          -p <path>       : Path to MaNGOS (default: /opt/mangos-<version>)
          -d              : Set in debug mode
          -j <number>     : Number of jobs for make (default 1)
          -v <version>    : Set MaNGOS version (classic|tbc|wotlk|cata)
          -h              : Print this help

This script does all steps to install MaNGOS depending on the GNU/Linux distribution :

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

All actions are logged in the mangos-installer.log file.

## Distributions

mangos-installer has been tested on several GNU/Linux distributions :

* Debian
 * Debian Stretch (9.x)
 * Debian Buster (10.x)
 * Debian Bullseye (11.x)
* Ubuntu
 * Ubuntu Bionic (18.04)
 * Ubuntu Focal (20.04)
 * Ubuntu Groovy (20.10)
 * Ubuntu Hirsute (21.04)
* Centos
 * CentOS 7.x
* Fedora

## Architecture

mangos-installer has been tested on several architectures :

* x86 (32 bits)
* x86_64 (64 bits)

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
