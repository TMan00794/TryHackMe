# TryHackMe -Easy Peasy


## Beginning Tasks - Start Up!


 1.) Log in to [TRY HACK ME](https://www.tryhackme.com)

 2.) Open a terminal in your Virtual Machine
     - ls into your *Documents* Directory
     - ls into your *tryhackme* Directory to locate your *"Open VPN Username"*
     - sudo openvpn {Your Username VPN}
     - *Leave this Terminal open in the background and open another terminal*

 3.) In your second terminal:
     - Download gobuster in your terminal by using *sudo apt install gobuster*
     - Use the following command with the IP from the TryHackMe website room:

           gobuster dir -w /usr/share/wordlist/dirbuster/directory-list-2.3-medium.txt -u *{IP Address from TryHackMe}*

 3.)

- Bullet?
- *Italisized*
