- Update
  - ```apt-get update && apt-get upgrade -y && apt-get dist-upgrade -y```
(update the list of available packages and their versions + install newer versions of the packages + install available updates for the OS release without updating OS to a higher version)
- Additional commands
  - ```apt-get install preload``` (daemon that runs in the background and analyzes user behavior and frequently run applications)
  - ```apt-get install bleachbit``` (disk space cleaner, privacy manager, and computer system optimizer)
  - ```apt-get install bum``` (boot-up manager)
  - ```apt-get install gnome-do``` (intelligent launcher that also allows to perform specific tasks on the search result)
  - ```apt-get install apt-file``` (searches available packages for a specific file or files. The packages do not need to be installed to perform the search)
  - ```apt-get install scrub``` (writes patterns on magnetic media to thwart data recovery)
  - ```apt-get install shutter``` (screenshot tool)
  - ```apt-get install figlet``` (a program for making large letters out of ordinary text)
- Generating new SSH keys
  ```
  cd /etc/ssh
  mkdir ssh_keys_backup
  mv ssh_host_* ssh_keys_backup
  dpkg-reconfigure openssh-server
  ```
  - ```service ssh start``` to start SSH
  - ```netstat -antp``` to verify the deamon is running
    - `-a`	This switch displays active TCP connections, TCP connections with the listening state, as well as UDP ports that are being listened to.
    - `-n`	Use the -n switch to prevent netstat from attempting to determine host names for foreign IP addresses. Depending on your current network connections, using this switch could considerably reduce the time it takes for netstat to fully execute.
    - `-p`	Use the -p switch to show connections or statistics only for a particular protocol. You can not define more than one protocol at once, nor can you execute netstat with -p without defining a protocol.
    protocol 	When specifying a protocol with the -p option, you can use tcp, udp, tcpv6, or udpv6. If you use -s with -p to view statistics by protocol, you can use icmp, ip, icmpv6, or ipv6 in addition to the first four I mentioned.
    - `-t`	Use the -t switch to show the current TCP chimney offload state in place of the typically displayed TCP state.

- Anonymous browsing
  - ```apt-get install tor```
  - edit `/etc/proxychains.conf`:
    - comment out `strict_chain`, uncomment `dynamic_chain`
  - ```service tor start```
  - ```proxychains firefox www.whatismyip.com```
 
