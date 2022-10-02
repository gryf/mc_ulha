=======================
Midnight Commander ulha
=======================

Midnight Commander extfs plugin for handling lha Amiga archives.

Description
-----------

ULha is an extfs plugin which can be used with lha/lzh/lharc archives.
Personally, I've use it almost exclusively for archives created long time ago
on my Amiga. Both reading from and writing into archive was implemented.

Requirements
------------

ULha requires `free lha <http://lha.sourceforge.jp>`_ implementation to work.

Installation
------------

* install `extfslib`_
* copy ``ulha`` to ``~/.local/share/mc/extfs.d/``
* add or change entry for files handle in ``~/.config/mc/mc.ext``::

    # lha
    regex/\.[lL]([Hh][aA]|[Zz][hH])$
         Open=%cd %p/ulha://
         View=%view{ascii} lha l %f

License
=======

This software is licensed under 3-clause BSD license. See LICENSE file for
details.


.. _extfslib: https://github.com/gryf/mc_extfslib
