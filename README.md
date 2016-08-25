![Ring](http://ring-lang.sourceforge.net/thering.jpg)

# Ring Programming Language

## Innovative and practical general-purpose multi-paradigm language

||*Resources*||*Status*|
|---|---|---|---|             																															 
|Download |[![Download](https://img.shields.io/badge/binary%20release-version%201.0-brightgreen.svg)](http://ring-lang.sourceforge.net/download.html)|**MacOS X (Compiler: gcc C)**      |[![Build Status](https://travis-ci.org/ring-lang/ring.png)](https://travis-ci.org/ring-lang/ring)|   
|Help |[![Help](https://img.shields.io/badge/documentation-version%201.0-orange.svg)](http://ring-lang.sourceforge.net/doc/index.html)|**Ubuntu Linux (Compiler: gcc C)** |[![Build Status](https://travis-ci.org/ring-lang/ring.png)](https://travis-ci.org/ring-lang/ring)|                  
|Try |[![Try](https://img.shields.io/badge/interactive%20ring-use%20online-green.svg)](http://ring-lang.sourceforge.net/cgi-bin/ringlang.cgi)|**MacOS X (Compiler: clang C)**      |[![Build Status](https://travis-ci.org/ring-lang/ring.png)](https://travis-ci.org/ring-lang/ring)|   
|Support |[![Support](https://img.shields.io/badge/group-ask%20questions-yellowgreen.svg)](https://groups.google.com/forum/#!forum/ring-lang)|**Ubuntu Linux (Compiler: clang C)** |[![Build Status](https://travis-ci.org/ring-lang/ring.png)](https://travis-ci.org/ring-lang/ring)|                  

=============
Description
=============

The Ring is an Innovative and practical general-purpose multi-paradigm scripting language that
can be embedded in C/C++ projects, extended using C/C++ code and/or used as standalone language.
The supported programming paradigms are Imperative, Procedural, Object-Oriented, Functional,
Meta programming, Declarative programming using nested structures, and Natural programming.
The language is portable (Windows, Linux, Mac OS X, Android, etc.) and can be used to create
Console, GUI, Web, Games and Mobile applications. 
The language is designed to be Simple, Small, Flexible and Fast. 
Its Dynamic Language (Dynamic Typing and Weakly Typed) that compile the source code to
byte code then execute it by the Ring Virtual Machine, which is integrated with the
Ring Compiler in one program. [Read more!](http://ring-lang.sourceforge.net/#why)

#Building from source code

You can build Ring using CMake or using Scripts (Batch Files or Shell Scripts).

The next steps explains building using scripts.

## Building using Microsoft Windows 

### Get the source code

	git clone http://github.com/ring-lang/ring.git
	
### Install Libraries 
	
	MySQL     : https://dev.mysql.com/downloads/connector/c/
	LibCurl   : https://curl.haxx.se/libcurl/
	OpenSSL   : https://www.openssl.org
	Allegro 5 : http://liballeg.org/download.html#windows
	Qt 5.5    : https://download.qt.io/archive/qt/5.5/5.5.1/
	
	You can quickly install MySQL, LibCurl, OpenSSL and Allegro libraries 
	from this link : https://sourceforge.net/projects/ring-lang/files/Ring%201.0/libdepwin.zip/download
	Then extract and copy the libraries folders to Ring/libdepwin
	
### Build Ring (Compiler/VM)
	
	cd ring/src
	buildvccomplete.bat
	
### Generate RingAllegro Source Code and Build 
	
	cd ../extensions/ringallegro
	gencode.bat
	buildvc.bat
	
### Generate RingQt Source Code and Build
	
	cd ../ringqt
	gencode.bat
	buildmingw32.bat

### To be able to call ring from any folder 
	
	cd ../../bin
	install.bat
	
#### Add Ring/bin to System path

	Hit "windows key".
	Type "Edit the System environment variables"
	Select "Advanced" tab.
	Click on "Enviroment Variables..."
	Double click on "Path"
	Add at the end the new path separated by semicolon. 
		;C:\Ring\Bin
	
### Run Ring Notepad
	
	cd applications/rnote
	ring rnote.ring

## Building using Ubuntu Linux 

### Get the source code

	git clone http://github.com/ring-lang/ring.git
	
### Install Libraries 
	
	cd ring/src
	./installdep.sh 
	
### Build Ring (Compiler/VM)
	
	sudo ./buildgcccomplete.sh
	
### Generate RingAllegro Source Code and Build 
	
	cd ../extensions/ringallegro
	./gencode.sh
	./buildgcc.sh

	
### Generate RingQt Source Code and Build
	
	cd ../ringqt
	./gencode.sh
	./buildgcc.sh

### To be able to call ring from any folder 
	cd ../../bin
	sudo ./install.sh
	
### Run Ring Notepad
	
	cd applications/rnote
	sudo ring rnote.ring

	
## Building using MacOS X

### Get the source code

	git clone http://github.com/ring-lang/ring.git
	
### Install homebrew (follow the directions on [homebrew's homepage](http://brew.sh/)).
	
### Install Libraries 
	
	brew install unixodbc mysql-connector-c allegro homebrew/versions/qt52
	
### Build Ring (Compiler/VM)
	
	cd ring/src
	./buildclangcomplete.sh
	
	
### Generate RingAllegro Source Code and Build 
	
	cd ../extensions/ringallegro
	./gencode.sh
	./buildclang.sh

	
### Generate RingQt Source Code and Build
	
	cd ../ringqt
	./gencode.sh
	./buildclang.sh

### To be able to call ring from any folder 
	cd ../../bin
	sudo ./install.sh
	
### Run Ring Notepad
	
	cd applications/rnote
	sudo ring rnote.ring
	

## Building using CMake 

Install libraries (MySQL Client, OpenSSL, LibCurl, Allegro 5 and Qt 5.5)

	cmake .
	make
