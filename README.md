# TryHackMe -Easy Peasy


## Beginning Tasks - Start Up!


**1.) Log in to [TRY HACK ME](https://www.tryhackme.com)**

**2.) Open a terminal in your Virtual Machine**
```
      ls into your *Documents* Directory

      ls into your *tryhackme* Directory to locate your {"Open VPN Username"}

      sudo openvpn {Your Username VPN}
```

**Leave this Terminal open in the background and open another terminal**


 **3.) Run nmap -A -p- {IP Address from TryHackMe}**

```
      - nmap : Nmap (“Network Mapper”) is an open source tool for network exploration and security
       auditing. It was designed to rapidly scan large networks, although it works fine against
       single hosts. Nmap uses raw IP packets in novel ways to determine what hosts are
       available on the network, what services (application name and version) those hosts are
       offering, what operating systems (and OS versions) they are running, what type of packet
       filters/firewalls are in use, and dozens of other characteristics. While Nmap is
       commonly used for security audits, many systems and network administrators find it
       useful for routine tasks such as network inventory, managing service upgrade schedules,
       and monitoring host or service uptime.

       The output from Nmap is a list of scanned targets, with supplemental information on each
       depending on the options used. Key among that information is the “interesting ports
       table”.  That table lists the port number and protocol, service name, and state. The
       state is either open, filtered, closed, or unfiltered.  Open means that an application
       on the target machine is listening for connections/packets on that port.  Filtered means
       that a firewall, filter, or other network obstacle is blocking the port so that Nmap
       cannot tell whether it is open or closed.  Closed ports have no application listening on
       them, though they could open up at any time. Ports are classified as unfiltered when
       they are responsive to Nmap's probes, but Nmap cannot determine whether they are open or
       closed. Nmap reports the state combinations open|filtered and closed|filtered when it
       cannot determine which of the two states describe a port. The port table may also
       include software version details when version detection has been requested. When an IP
       protocol scan is requested (-sO), Nmap provides information on supported IP protocols
       rather than listening ports.

       In addition to the interesting ports table, Nmap can provide further information on
       targets, including reverse DNS names, operating system guesses, device types, and MAC
       addresses.
```
                                          Source: Kali Linux Terminal MAN Pages
```
      - -A :(Aggressive scan options)

           This option enables additional advanced and aggressive options. Presently this
           enables OS detection (-O), version scanning (-sV), script scanning (-sC) and
           traceroute (--traceroute).  More features may be added in the future. The point is
           to enable a comprehensive set of scan options without people having to remember a
           large set of flags. However, because script scanning with the default set is
           considered intrusive, you should not use -A against target networks without
           permission. This option only enables features, and not timing options (such as -T4)
           or verbosity options (-v) that you might want as well. Options which require
           privileges (e.g. root access) such as OS detection and traceroute will only be
           enabled if those privileges are available.
```
                                        Source: Kali Linux Terminal MAN Pages
```
      - -p- : port ranges (Only scan specified ports)
           This option specifies which ports you want to scan and overrides the default.
           Individual port numbers are OK, as are ranges separated by a hyphen (e.g.  1-1023).
           The beginning and/or end values of a range may be omitted, causing Nmap to use 1 and
           65535, respectively. So you can specify -p- to scan ports from 1 through 65535.
           Scanning port zero is allowed if you specify it explicitly. For IP protocol scanning
           (-sO), this option specifies the protocol numbers you wish to scan for (0–255).
```
                                        Source: Kali Linux Terminal MAN Pages



 **4.) In your second terminal:**
     - Download gobuster in your terminal by using *sudo apt install gobuster*
     - Use the following command with the IP from the TryHackMe website room:

           gobuster dir -w /usr/share/wordlist/dirbuster/directory-list-2.3-medium.txt -u *{IP Address from TryHackMe}*

 **5.) While waiting on the results from the gobuster command, type in dirbuster in your VM**
    - dirbuster -H -u http://{IP Address from TryHackMe} -t 200 -l /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt 


- Bullet?
- *Italisized*
