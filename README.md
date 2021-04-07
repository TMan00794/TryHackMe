# TryHackMe -Easy Peasy


## Beginning Tasks - Start Up!


 1.) Log in to [TRY HACK ME](https://www.tryhackme.com)

 2.) Open a terminal in your Virtual Machine
```
      ls into your *Documents* Directory

      ls into your *tryhackme* Directory to locate your *"Open VPN Username"*

      sudo openvpn {Your Username VPN}

      *Leave this Terminal open in the background and open another terminal*
```
 3.) Run nmap -A -p- *{IP Address from TryHackMe}*

      - nmap :

      - -A :(Aggressive scan options)
```
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

      - -p- : port ranges (Only scan specified ports)
           This option specifies which ports you want to scan and overrides the default.
           Individual port numbers are OK, as are ranges separated by a hyphen (e.g.  1-1023).
           The beginning and/or end values of a range may be omitted, causing Nmap to use 1 and
           65535, respectively. So you can specify **-p- to scan ports from 1 through 65535.**
           Scanning port zero is allowed if you specify it explicitly. For IP protocol scanning
           (-sO), this option specifies the protocol numbers you wish to scan for (0–255).




 4.) In your second terminal:
     - Download gobuster in your terminal by using *sudo apt install gobuster*
     - Use the following command with the IP from the TryHackMe website room:

           gobuster dir -w /usr/share/wordlist/dirbuster/directory-list-2.3-medium.txt -u *{IP Address from TryHackMe}*

 3.)

- Bullet?
- *Italisized*
