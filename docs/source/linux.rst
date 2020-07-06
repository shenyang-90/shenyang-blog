
Linux OS
========


Useful Command
--------------


.. code::

   find . -name '*.swp' -type f -print -delete

   mount -t auto /dev/cdrom /mnt/cdrom

   find . -name * | wc -l

   sed -i "s/oldstring/newstring/g" `grep oldstring -rl yourdir`

   od -h xxx.bin



Compress and Uncompress
-----------------------

.. code::

   tar -xvf xxx.tar

   tar -czvf xxx.tar.gz xxx

   jzip -d xxx.gz

   xz -d xxx.tar.xz


.. note::

   1. *.tar - tar -xvf

   #. *.gz - gzip -d or gunzip

   #. *.tar.gz or *.tgz - tar -xzf

   #. *.bz2 - bzip2 -d or bunzip2

   #. *.tar.bz2 -tar -xjf

   #. *.Z - uncompress

   #. *.tar.Z - tar -xZf

   #. *.rar - unrar

   #. *.zip - unzip



VIM
---

Plug - EasyAlign
++++++++++++++++

**Download** https://github.com/junegunn/vim-easy-align

1. vipga
#. `=` or `Ctrl + x`



