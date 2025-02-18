Perl IRC Statistics Generator (pisg) is a Perl script which takes IRC
logfiles and turns them into nice looking stats, which can be amusing to
show for the users of your channel.

The supported logfile formats is explained in the FORMATS file included with
this distribution in the 'docs' directory.

SETTING UP PISG
---------------
Full documentation for pisg is located in 'docs/pisg-doc.txt' and
'docs/html/index.html' for a HTML version.

Quick usage instructions below:

Install URI::Find::Schemeless first.

It's quite simple to set up pisg. You have 2 choices:

 * Set settings from commandline (try pisg --help)
 * Configure pisg from the pisg.cfg file (more flexible and configurable)

If you look in the example pisg.cfg, you will see a small working sample
where you can insert your own data.

The commandline version has the disadvantage that you can only set up one
channel to be run.

RUNNING PISG
------------
With ZNC, you might need to use this: 
/msg *status loadmod log -sanitize /home/YOURUSER/.znc/users/YOURUSER/moddata/log/$NETWORK/$WINDOW.log
(edit YOURUSER) with your own info. This will enable logging in a clean way for PISG to read them

If you have setup everything inside the config file, then you just need to
run it. If you're on a Linux/BSD/Unix system, this should do the work:

    $ ./pisg

Running pisg like this will just use the settings in pisg.cfg.

If you want to specify things on commandline instead of in the config file,
you could do:

    $ ./pisg -ch \#channel -l logfile.log -f mIRC -o index.html
   
The syntax and options is explained when doing:

    $ ./pisg --help

Setting settings on commandline, will override the relevant settings in
pisg.cfg.

NOTES
-----
There is some graphics in the gfx/ folder which pisg uses, you should put
these in the same directory as your stats file(s) or use the 'PicLocation'
configuration option.

The stats will look best with a logfile which is at least one day long.
Some stats (like smilies, exclamation marks, etc) doesn't get counted before
a special amount of time.

pisg supports multiple languages so the texts on the stats page will
be in your own language; look in lang.txt to see the supported languages.
The language can be changed from within the pisg.cfg file.

If you have any corrections to the language file, or you want to add a new
translation, then send it to the mailing list.

CONTACT INFORMATION
-------------------
If you have any issues with pisg, such as problems with installing or
running pisg, then join us on the freenode IRC Network: chat.freenode.net on #pisg

The pisg homepage is located at http://pisg.github.io/.

Have fun :)
