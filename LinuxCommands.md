| **Category** | **Command** | **Sample** | **Explanation** |
|---|---|---|---|
| Navigation | `ls` | `ls -la /var/log` | List directory contents; show hidden files and permissions |
| Navigation | `cd` | `cd /var/log` | Change current directory |
| Navigation | `pwd` | `pwd` | Print current working directory |
| File viewing | `cat` | `cat /etc/hosts` | Print file contents to stdout |
| File viewing | `less` | `less /var/log/syslog` | Page through large files; search and navigate |
| File viewing | `tail` | `tail -n 200 /var/log/auth.log` | Show last lines; use `-f` to follow live updates |
| Text search | `grep` | `grep -R "Failed password" /var/log` | Search text patterns recursively |
| Text processing | `awk` | `awk '{print $1,$2}' file` | Extract and format fields from text |
| Text processing | `sed` | `sed -n '1,50p' file` | Stream editor for extraction and transforms |
| File discovery | `find` | `find / -type f -mtime -1` | Locate files by name, type, or modification time |
| File discovery | `locate` | `locate passwd` | Fast filename lookup using a database |
| File inspection | `file` | `file /usr/bin/ssh` | Determine file type (binary, script, text) |
| Process inspection | `ps` | `ps aux \| grep sshd` | Snapshot of running processes |
| Process monitoring | `top` | `top` | Live CPU and memory view |
| Process monitoring | `htop` | `htop` | Enhanced interactive process viewer (if installed) |
| Open files & sockets | `lsof` | `lsof -i :22` | List open files and network sockets |
| Network sockets | `ss` | `ss -tunap` | Show listening and established sockets |
| Network config | `ip` | `ip addr show` | Show or configure network interfaces and addresses |
| Packet capture | `tcpdump` | `tcpdump -i eth0 -w capture.pcap` | Capture packets for analysis |
| Packet analysis | `tshark` | `tshark -r capture.pcap` | CLI packet analysis using Wireshark engine |
| System logs | `journalctl` | `journalctl -u sshd --since "1 hour ago"` | Query systemd journal logs |
| Services | `systemctl` | `systemctl status sshd` | Inspect and control systemd services |
| Authentication history | `last` | `last -n 20` | Show recent logins |
| User presence | `who` | `who` | Show currently logged-in users |
| Host info | `uname` | `uname -a` | Show kernel and OS details |
| Web requests | `curl` | `curl -I https://example.com` | Fetch HTTP headers and test endpoints |
| Downloads | `wget` | `wget https://example.com/file` | Download files from the web |
| Secure copy | `scp` | `scp file user@host:/tmp/` | Copy files over SSH for evidence collection |
| Sync & transfer | `rsync` | `rsync -avz src/ dest/` | Efficient local/remote file synchronization |
