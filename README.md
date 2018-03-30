Hostile
=======

Hostile is a simple autosetup script for Steven Black's hostname blacklist.

(See https://github.com/StevenBlack/hosts for more information)

Usage
-----

1. Copy your existing /etc/hosts into a new file /etc/hosts.custom. Use this
for all future manual changes to /etc/hosts.

2. Run update-hosts.sh as root or via sudo to create a new /etc/hosts file
containing both your /etc/hosts.custom config, and the blacklist domains.

3. Re-run update-hosts.sh whenever you like to pull in the latest changes.
Make sure never to edit /etc/hosts by hand - all future changes go in
/etc/hosts.custom.

Recommendations
---------------

I've symlinked update-hosts.sh into /usr/local/sbin, and set up an anacron job
to run it daily to ensure I always have the latest copy.
