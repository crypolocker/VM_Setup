| **Category** | **Windows** | **PowerShell (Windows)** | **Linux** | **Notes** |
|---|---|---|---|---|
| IP Configuration | `ipconfig` | `Get-NetIPConfiguration` | `ip addr` / `ifconfig` | Displays basic IP configuration for network interfaces |
| IP Configuration | `ipconfig /all` | `Get-NetIPConfiguration` | `ip addr show` | Shows detailed network configuration including MAC, DHCP, and DNS |
| IP Configuration | `ipconfig /release` | `Release-DhcpLease` | `dhclient -r` | Releases the IP address obtained from a DHCP server |
| IP Configuration | `ipconfig /renew` | `Renew-DhcpLease` | `dhclient` | Requests a new IP address from the DHCP server |
| IP Configuration | `ipconfig /flushdns` | `Clear-DnsClientCache` | `systemd-resolve --flush-caches` | Clears the local DNS resolver cache |
| Connectivity Testing | `ping` | `Test-Connection` | `ping` | Tests network connectivity using ICMP echo requests |
| Connectivity Testing | `ping -n <count>` | `Test-Connection -Count <count>` | `ping -c <count>` | Sends a specified number of ICMP echo requests |
| Path Analysis | `tracert` | `Test-NetConnection -TraceRoute` | `traceroute` | Traces the route packets take to a destination host |
| Path Analysis | `tracert -d` | `Test-NetConnection -TraceRoute` | `traceroute -n` | Traces the route without DNS resolution |
| DNS Troubleshooting | `nslookup` | `Resolve-DnsName` | `nslookup` / `dig` | Queries DNS servers to resolve domains or IPs |
| Connection Monitoring | `netstat` | `Get-NetTCPConnection` | `ss` / `netstat` | Displays active TCP connections and listening ports |
| Connection Monitoring | `netstat -an` | `Get-NetTCPConnection` | `ss -an` | Shows all connections and ports in numeric form |
| Connection Monitoring | `netstat -b` | `Get-NetTCPConnection` + `Get-Process` | `ss -p` | Identifies the process using a network connection |
| Connection Monitoring | `netstat -o` | `Get-NetTCPConnection` | `ss -p` | Displays process IDs associated with connections |
| Routing | `netstat -r` | `Get-NetRoute` | `ip route` | Displays the system routing table |
| Address Resolution | `arp` | `Get-NetNeighbor` | `ip neigh` / `arp` | Manages and displays ARP cache entries |
| Address Resolution | `arp -a` | `Get-NetNeighbor` | `ip neigh show` | Displays IP-to-MAC address mappings |
| Address Resolution | `arp -d <IP>` | `Remove-NetNeighbor` | `ip neigh del <IP>` | Deletes a specific ARP cache entry |
| Routing | `route print` | `Get-NetRoute` | `ip route show` | Displays the local IP routing table |
| System Identification | `hostname` | ``$env:COMPUTERNAME`` | `hostname` | Displays the system hostname |
| Network Diagnostics | `pathping` | `Test-NetConnection -TraceRoute` | `mtr` | Identifies packet loss and latency across hops |
| Hardware Information | `getmac` | `Get-NetAdapter` | `ip link` | Displays MAC addresses of network adapters |
| Network Configuration | `netsh` | `Get-NetIPInterface` | `nmcli` / `ip link` | Configures and displays network interface settings |
| Network Configuration | `netsh interface ipv4 show config` | `Get-NetIPConfiguration` | `ip addr show` | Displays IPv4 configuration for interfaces |
| Firewall Management | `netsh advfirewall show allprofiles` | `Get-NetFirewallProfile` | `ufw status` / `iptables -L` | Displays firewall profile status |
| Firewall Management | `netsh advfirewall firewall show rule name=all` | `Get-NetFirewallRule` | `iptables -L` / `nft list ruleset` | Lists configured firewall rules |
| NetBIOS Troubleshooting | `nbtstat` | `Get-WmiObject Win32_NetworkAdapterConfiguration` | `nmblookup` | Displays NetBIOS-related information |
| Network Shares | `net view` | `Get-SmbShare` | `smbclient -L` | Displays available shared resources |
| Network Shares | `net use` | `New-SmbMapping` | `mount -t cifs` | Connects to or disconnects from shared network resources |
| Network Testing | `telnet` | `Test-NetConnection -Port <port>` | `nc` / `telnet` | Tests TCP port connectivity |
| Network Testing | `ftp` | `Invoke-WebRequest` / `Start-BitsTransfer` | `ftp` / `curl` / `wget` | Transfers files using FTP or HTTP-based methods |
