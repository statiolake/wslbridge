# Version 0.2.3 (2017-06-30)

Changes since 0.2.2

 * Binaries are linked with -static-libgcc and -static-libstdc++.

 * Build the binaries with an Ubuntu 14.04 WSL installation.  The binaries
   for 0.2.2 were built with Ubuntu 16.04, and do not work on 14.04.

# Version 0.2.2 (2017-06-23)

Changes since 0.2.1

 * Fix a race condition affecting spawn failure.

 * Capture and report errors from the Microsoft Bash Launcher (bash.exe).
   In particular, don't hang if the user tries to simultaneously run elevated
   and non-elevated WSL instances.
   [#13](https://github.com/rprichard/wslbridge/issues/13)

# Version 0.2.1 (2016-11-14)

Changes since 0.2.0

 * The frontend now synchronizes the Cygwin environment with the Win32
   environment before creating the WSL backend process.
   https://github.com/mintty/wsltty/issues/14

# Version 0.2.0 (2016-09-28)

Changes since 0.1.0:

 * Added a `-C` option that changes the working directory before running the
   command.  The argument is a WSL path.  A `~` component at the start of the
   argument is replaced with the user's home directory.  (i.e. `$HOME`).
   [#2](https://github.com/rprichard/wslbridge/issues/2)

 * The frontend now canonicalizes its path to the `wslbridge-backend` binary.
   [#4](https://github.com/rprichard/wslbridge/issues/4)

# Version 0.1.0 (2016-08-17)

Initial release
