Doit - fire-and-forget script mailer
====================================

Copyright 2020-2022 Michael D Labriola <veggiemike@sourceruckus.org>

Licensed under the GPLv3. See the file COPYING for details. 

Doit executes a command in the background and mails its output and exit status
to a specified account.  It can also log to a file locally instead of mailing,
if that's what floats your boat.

Get the latest and greatest from https://github.com/sourceruckus/doit.

<pre>
usage: doit OPTIONS CMD...

  -h, --help                Show this help message and exit.

  -V, --version             Show version string and exit.

  -f, --filename LOGFILE    Specify output filename.  Both stdout and stderr
                            will be redirected to this file.  When the process
                            finishes, the files last few lines will contain
                            "DOIT: ALL DONE", a return code, and timing stats.

  -m, --mail EMAILADDRESS   Email stdout/stderr to specified address instead
                            of logging to a file.

  -a, --attachment          Send output as an attachment instead of as the email
                            body.  The exit status and timing info will remain
                            in email body.

NOTE: If CMD contains any arguments (e.g., -f, --verbose), you'll need to
      separate it from the rest of the doit commandline via -- (the special
      getopt stop parsing flag).

NOTE: If CMD is a compound statement, you'll need to quote and escape things
      appropriately.

example: doit --mail me@myemail.com --attachment -- kernel-builder --stable

example: doit -f ~/build.log -- \
           "find /boot -type f -exec echo {} \; -exec sleep .1 \; && echo woot"
</pre>
