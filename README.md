# Introduction
This script (try) run a command multiple times with an interval if the command fails for the first time.
Whenever the exit status of the running command return 0, the script doesn't continue any more.
_____________________________________________________________________________________________________

# How to

Usage: try [options] COMMAND

Execute a command repeatedly

Options:

-i num, 	interval between repetition (Default: 5)

-n num,		number of repetition (Default: 12)

-h 		help

Also you're able to set Environment variables instead of options.

TRY_INTERVAL=	interval between repetition (Default: 5)

TRY_NUMBER=	number of repetition (Default: 12)

TRY_COMMAND=	the command that you want to execute
____________________________________________________________________________________________________

Exit status:

0	ok

1	unsuccessful

2	command is not specified by input or Environment variable.
_____________________________________________________________________________________________________
Sample:

try -i 2 -n 5 ls -l

try -n 4 ping -c 2 4.2.2.4

try ls -l

TRY_COMMAND="telnet localhost 25" try

_____________________________________________________________________________________________________

# contribute

You are able to improve the sccript functionality in different environment.





[@dwsclass](https://github.com/dwsclass) dws-dev-002-bash
