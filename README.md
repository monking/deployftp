deployftp
=========

For when you have no other choice. Uses `bash`, `ftp`, `sum`, and  `git`.

Installation
------------

It's recommended to create an alias for the executable. Add this to your
`.bash_alias`, `.bashrc`, or `.bash_alias` file, changing the part in CAPS to
point to the location of this directory:

	alias deployftp /PATH/TO/deployftp/bin/deployftp

Usage
-----

Have your FTP server information handy the first time you run `deployftp`.
You'll need your **host**, **username**, **password**, and the **absolute path
of your web root**.

You'll be prompted for all relevant information. If you choose to let
`deployftp` save your password, it will be stored in clear text. Anyone with
access to the directory where you installed deployftp will be able to read your
password.

You'll also be asked for the "Assets path." This defaults to
`*/wp-content/uploads/*`, a pattern to find the uploads folder in a WordPress
site, but you can change it to any path. This is useful if your Git working
copy is ignoring an assets, uploads, or media directory that you want to
upload. The path is really a pattern compatible with the `find` utility, which
will match all the files that you want to upload apart from the Git tracked
files.

Caveats
-------

deployftp does not create any backups of your remote data. It is suggested that
you archive your live site before deploying. 
