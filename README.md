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

You'll also be asked for the **assets path**, which is used in a `find -path`
search to match the contents of a directory your Git working copy is ignoring.
The default (`*/wp-content/uploads/*`) looks for a WordPress uploads directory.

Caveats
-------

deployftp does not create any backups of your remote data. It is suggested that
you archive any files that will be overwritten by deploying.

Please test your setup by supplying a temporary remote webroot path. When you're satisfied
that everything was delivered correctly to that directory, you can edit the
`cases/<case_name>ftp_config` file to define `ftp_root` as the real webroot.
