# Python-Network-Tools
_Just some network tools written in Python_

## Nettools.py
_A netcat replacement that I wrote inspired by reading Justin Seitz's book "Black Hat Python: Python Programming for Hackers and Pentesters"_

```
Usage: nettools.py -t target_host -p port
-l --listen                - listen on [host]:[port] for incoming connections
-e --execute=file_to_run   - execute the given file upon receiving a connection
-c --command               - initialize a command shell
-u --upload=destination    - upon receiving connection upload a file and write to [destination]
Examples: 
nettools.py -t 192.168.0.1 -p 5555 -l -c
nettools.py -t 192.168.0.1 -p 5555 -l -u=c:\\target.exe
nettools.py -t 192.168.0.1 -p 5555 -l -e=\"cat /etc/passwd\"
echo 'ABCDEFGHI' | ./nettools.py -t 192.168.11.12 -p 135
```
