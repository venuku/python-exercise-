# Note: I did not have much time to complete unit test cases, I created a folder called test folder. In the project strucutre, this folder will have unit test cases.

# Pre-Requisities:
Python 3

# execution command:
For running this project, in your terminal run following command.

```
python3 src/app.py "../assets/commands.dat"
```


# Problem Explanination:

- Before installing a package, automatically install all the packages it requires.

- Before removing a package, confirm that no other packages require it. Dependent packages must be removed manually before the package can be removed.

Input



The input received by your program will contain a sequence of commands, each on a separate line, containing no more than eighty characters. The command names (DEPEND, INSTALL, REMOVE, and LIST) always appear in uppercase starting in column one and the command line separator is one or more spaces. All appropriate DEPEND commands will appear before the occurrence of any INSTALL dependencies. The end of the input is marked by a line containing only the word END.



Command Syntax


DEPEND item1 item2 [item3]       Package item1 depends on package item2 (and item3 or any additional packages).

INSTALL item1                    Installs item1 and any other packages required by item1.

REMOVE item                      Removes item1 and, if possible, packages required by item1.

LIST                             Lists the names of all currently installed packages.

END                              Marks the end of input, when used in a line by itself.





Output



The input received by your program will contain a sequence of commands, each on a separate line, containing no more than eighty characters. The command names (DEPEND, INSTALL, REMOVE, and LIST) always a



1. Echo each line of input.

2. Follow each echoed INSTALL or REMOVE line with the actions taken in response, making certain that the actions are given in the proper order.

3. For the LIST command, display the names of the components currently installed.

4. For the DEPEND and END commands, no output, except the echo, is produced.

5. For the DEPEND command, there will only be one dependency list per item.





STDIN



DEPEND TELNET TCPIP NETCARD
DEPEND TCPIP NETCARD
DEPEND DNS TCPIP NETCARD
DEPEND BROWSER TCPIP HTML
INSTALL NETCARD
INSTALL TELNET
INSTALL foo
REMOVE NETCARD
INSTALL BROWSER
INSTALL DNS
LIST
REMOVE TELNET
REMOVE NETCARD
REMOVE DNS
REMOVE NETCARD
INSTALL NETCARD
REMOVE TCPIP
REMOVE BROWSER
REMOVE TCPIP
LIST
END




STDOUT



DEPEND TELNET TCPIP NETCARD
DEPEND TCPIP NETCARD
DEPEND DNS TCPIP NETCARD
DEPEND BROWSER TCPIP HTML
INSTALL NETCARD
NETCARD successfully installed
INSTALL TELNET
TCPIP successfully installed
TELNET successfully installed
INSTALL foo
foo successfully installed
REMOVE NETCARD
NETCARD is still needed.
INSTALL BROWSER
HTML successfully installed
BROWSER successfully installed
INSTALL DNS
 DNS successfully installed
LIST
HTML
BROWSER
DNS
NETCARD
foo
TCPIP
TELNET
REMOVE TELNET
TELNET successfully removed
REMOVE NETCARD
NETCARD is still needed
REMOVE DNS
DNS successfully removed
REMOVE NETCARD
NETCARD is still needed
INSTALL NETCARD
NETCARD is already installed
REMOVE TCPIP
TCPIP is still needed
REMOVE BROWSER
BROWSER successfully removed
HTML is no longer needed
HTML successfully removed
TCPIP is no longer needed
TCPIP successfully removed
REMOVE TCPIP
TCPIP is not installed
LIST
NETCARD
foo
END 
