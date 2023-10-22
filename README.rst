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

ULha requires free `lha`_ implementation to work. There is another lha
implementation under development - `lhasa`_, although it is currently limited
to list and extract only.

Limitations
-----------

For filenames which contain other characters outside of ASCII set, there is no
way to operate on them as `lha`_ simply ignore those files. Extracting full
archive will extract also those files, although names would be incorrectly
decoded, and hence, unusable on the AmigaOS. Looking forward for the `lhasa`_
to be completed, and then will switch to it.

Installation
------------

* install `extfslib`_
* copy ``ulha`` to ``~/.local/share/mc/extfs.d/``
* add or change entry for files handle in ``~/.config/mc/mc.ext``:

.. code::ini

   [lha]
   Type=^LHa\ .*archive
   Open=%cd %p/ulha://
   View=%view{ascii} /usr/libexec/mc/ext.d/archive.sh view lha

License
=======

This software is licensed under 3-clause BSD license. See LICENSE file for
details.


.. _extfslib: https://github.com/gryf/mc_extfslib
.. _lha: http://lha.sourceforge.jp
.. _lhasa: https://github.com/fragglet/lhasa
