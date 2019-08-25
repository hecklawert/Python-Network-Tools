# Python-Network-Tools
_Just some network tools written in Python_

## Nettools.py
A netcat replacement that I wrote inspired by reading Justin Seitz's book "Black Hat Python: Python Programming for Hackers and Pentesters"

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

## pyproxy.py
There are a number of reasons to have a TCP proxy in your tool belt, both for forwarding traffic to bounce from host to host, but also when assessing network-based software. When performing penetration tests in enterprise environments, you’ll commonly be faced with the fact that you can’t run Wireshark, that you can’t load drivers to sniff the loopback on Windows, or that network segmentation prevents you from running your tools directly against your target host.

```
Usage: ./pyproxy.py [localhost] [localport] [remotehost] [remoteport] [receive_first]
Example: ./pyproxy.py 127.0.0.1 9000 10.12.132.1 9000 True
``` 
