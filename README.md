
this script run a command if its failed in first time, multiple times in an interval.

Usage: try [options] COMMAND

execute a command repeatedly

Options:

-i num, 	interval between repetition (Default: 5)
-n num,		number of repetition (Default: 12)
-h 		help

Also you're able to set Environment variables instead

TRY_INTERVAL	interval between repetition (Default: 5)
TRY_NUMBER	number of repetition (Default: 12)
TRY_COMMAND	the command that you want to execute

Exit status:
0	ok
1	unsuccessful
2	command is not specified by input or Environment variable.

Sample:

try -i 2 -n 5 ls -l

try -n 4 ping -c 2 4.2.2.4

try ls -l

TRY_COMMAND="telnet localhost 25" try


Note:
if you're using commands with more than 3 arguments you must use Environment variable.







[@dwsclass](https://github.com/dwsclass) dws-dev-002-bash
