# Ruby RPM spec
RPM spec file to build a ruby package

## Usage
Install packages to build RPMs in general:

    sudo yum -y install rpmdevtools


Install libary packages:

    sudo yum -y install glibc-devel readline-devel libyaml-devel ncurses-devel gdbm-devel tcl-devel openssl-devel db4-devel libffi-devel


Install some development tools:

    sudo yum -y install make gcc unzip byacc


Create build environment for RPMs:

    mkdir -p rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}
    cd rpmbuild


Get the spec file and ruby sources:

    wget https://github.com/innotronic/ruby/raw/master/ruby.spec -O SPECS/ruby.spec
    wget https://cache.ruby-lang.org/pub/ruby/2.2/ruby-2.2.3.tar.gz -O SOURCES/ruby-2.2.3.tar.gz


Build the RPM

    rpmbuild -ba SPEC/ruby.spec


Have fun with [ruby](http://ruby-lang.org/) ;-)

## License
Copyright (c) 2016 [Innotronic Ingenieurbüro GmbH](https://www.inno.ch/)

Based on prior work from [Nathan Milford](https://github.com/nmilford/rpm-ruby)

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

