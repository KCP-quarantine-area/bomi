# bomi
A powerful, easy-to-use Qt5 GUI multimedia player based on mpv.

http://bomi-player.github.io/

The only package needed from KCP for bomi to successfully build is libchardet.
-https://github.com/KaOS-Community-Packages/libchardet
Simply use the KCP helper in Octopi in order to download+install libchardet.

Beyond that, all other needed dependencies are in the official repositories.

Installation instructions (if not using the KCP helper):
-download+extract .zip file to a directory (~/Builds/bomi-master, for example)
-navigate to the directory in which the file is extracted
-run makepkg -si
