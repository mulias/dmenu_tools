Dmenu Tools
===========

A collection of small scripts using [dmenu](http://tools.suckless.org/dmenu/), a simple menu building tool.
The default functionality of dmenu is dmenu_run, which lets the user select and launch programs that are in the path.

In most cases, a dmenu script takes the output of a command, formats this output as a newline separated list, pipes the list into dmenu, has the user select a list item, then runs a command on the selected item. Dmenu is a convenient intermediary step for a user to select what they want to operate on.

I have absolutely no idea what I'm doing with bash, but all of these scripts run on my system. I can't promise anything more than that. I'm using dmenu2, which is a patched version of dmenu with xft font support and height, allowing for multiple rows.

Notes
-----
dexit  
Shut down, sleep, or hibernate the system, or shut down xwindows and return to the terminal. Uses the systemd session manager, systemctl. On a non-systemd system one would need commands such as "shutdown -h 0" available without sudo.

dfinder  
Search the home directory tree for files containing a search string. Very primitive search functionality, nothing fancy like fuzzy select. Uses find, which does not use an indexed database, but searches the entire given path every time. Someone with lots of files or a slow disk could change the search command to locate. 

dfiles
File browser.

dmenu_freq  
Launch binaries through dmenu. Pin most used applications so that they appear first in the dmenu search list. Launch with gksudo by appending '!' to the command, launch in a terminal by appending ';', and launch in a terminal with sudo by appending both.
