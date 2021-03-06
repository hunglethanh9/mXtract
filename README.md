# mXtract
[![Build Status](https://travis-ci.org/rek7/mXtract.svg?branch=master)](https://travis-ci.org/rek7/mXtract) [![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/rek7/mXtract/blob/master/LICENSE) [![Twitter](https://img.shields.io/badge/twitter-%40mxtract-blue.svg)](https://twitter.com/mxtract)
----
mXtract is an opensource linux based tool that analyzes and dumps memory. It is developed as an offensive pentration testing tool, its primary purpose is to scan memory for private keys, ips, and passwords using regexes. Remember, your results are only as good as your regexes.
## Screenshots
![Screenshot](https://github.com/rek7/mXtract/blob/master/img/ss1.png)

Scan with verbose and with a simple IP regex, scanning every data segment, displaying process info and scanning environment files.
![Screenshot](https://github.com/rek7/mXtract/blob/master/img/ss2.png)

Scan with verbose and with a simple IP regex, scanning only heap and stack, displaying process info and scanning environment files.
![Screenshot](https://github.com/rek7/mXtract/blob/master/img/ss3.png)

Scan without verbose, and with a simple IP regex, displaying process info and scanning environment files.
## Why dump directly from memory?
In most linux environments users can access the memory of processes, this allows attackers to harvest credentials, private keys, or anything that isnt suppose to be seen but is being processed by a program in clear text.
## Features
+ Ability to enter regex lists
+ Clear and Readable Display
+ Ability to Mass Scan Every Proccess or a Specific PID
+ Able to choose memory sections to scan
+ Ability to Show Detailed Process Information
+ Ability to Scan Process Environment Files
+ Memory dumps automatically removes unicode characters which allows for processing with other tools or manually
## Getting started
###### Downloading: ```git clone https://github.com/rek7/mXtract``` 
###### Compiling: ```cd mXtract && sh compile.sh``` 
###### This will create the directory bin/ and compile the binary as mXtract
## Commands 
```
General:
        -v      Enable Verbose Output
        -s      Suppress Banner
        -h      Help
        -c      Suppress Colored Output
Target and Regex:
        -i      Show Detailed Process/User Info
        -a      Scan all Memory Ranges not just Heap/Stack
        -e      Scan Process Environment Files
        -r=     Regex Database to Use
        -p=     Specify Single PID to Scan
Output:
        -wm     Write Raw Memory to File Default Directory is: 'pid/'
        -wi     Write Process Info to Beginning of File (Used in Conjunction with -w)
        -wr     Write Regex Output to File (Will Appear in the Output Directory)
        -f=     Regex Results Filename Default is: 'regex_results.txt'
        -d=     Custom Ouput Directory
```
