How to a add submodule
=======================
go to git root dir

and add (e.g for lusty)= git submodule add git://github.com/sjbach/lusty.git vim/bundle/lusty

After you add submodule you need register it, using

git submodule init

(inside the submodule dir)

Quick installation
==================
Simply run this script to install and configure this vimrc in your `$HOME`
dir::

make sure you have a ~/project folder first

	wget -O - https://github.com/gavriguy/vimrc/raw/master/autoinstall.sh | sh

Installing this vimrc manually
==============================
Although a vimrc is a very personal thing, you may use mine if you
like it.  To do so, please do the following:

1. Clone this repo::

   	git clone git://github.com/gavriguy/vimrc.git

   or download the plain source only::

   	wget -qO - http://github.com/gavriguy/vimrc/tarball/master | tar -xzvf -

2. In your ~/.vimrc, add the following line::

   	source ~/path/to/vimrc/vimrc

3. Fetch submodules::

   	git submodule init
   	git submodule update

4. Recompile Command-T Ruby C extension for your platform (if other than
   Mac OS X)::

   	cd vim/ruby/command-t
   	ruby extconf.rb
   	make clean; make

5. Touch::

   	touch ~/.vim/user.vim

That's it.
