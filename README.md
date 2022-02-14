# Zacky_PayGen
A simple and usage payload generator tool for educational purposes.


A **quick** way to generate various "basic" Meterpreter payloads via `msfvenom` (part of the Metasploit framework).

<p align="center">
  <img src="https://img.fruugo.com/product/3/64/175799643_max.jpg" alt="Zacky_logo"/>
</p>


- - -


## About

MSFvenom Payload Creator to generate multiple types of payload.

**Fully automating**
The rest is to make the user's life as **easy as possible** 
**Note** 
If you want to bypass Antivirus see for more of my tools :)

- - -


## Install

+ Designed for **Kali Linux v2.x/Rolling** & **Metasploit v4.11+**.

```
$ sudo git clone https://github.com/Gesus-del/Zacky_PayGen/edit/Zacky_PayGen
$ chmod +x /usr/local/bin/Zacky_PayGen
```
### Kali-Linux

```
$ sudo bash Zacky_PayGen.sh                  
 [*] MSFvenom Payload Creator (Zacky_PayGen v0.1)

 [i] Missing TYPE or BATCH/LOOP mode

 Zacky_PayGen.sh <TYPE> (<DOMAIN/IP>) (<PORT>) (<CMD/MSF>) (<BIND/REVERSE>) (<STAGED/STAGELESS>) (<TCP/HTTP/HTTPS/FIND_PORT>) (<BATCH/LOOP>) (<VERBOSE>)
   Example: Zacky_PayGen.sh windows 192.168.1.10        # Windows & manual IP.
            Zacky_PayGen.sh elf bind eth0 4444          # Linux, eth0's IP & manual port.
            Zacky_PayGen.sh stageless cmd py https      # Python, stageless command prompt.
            Zacky_PayGen.sh verbose loop eth1           # A payload for every type, using eth1's IP.
            Zacky_PayGen.sh msf batch wan               # All possible Meterpreter payloads, using WAN IP.
            Zacky_PayGen.sh help verbose                # Help screen, with even more information.

 <TYPE>:
   + APK
   + ASP
   + ASPX
   + Bash [.sh]
   + Java [.jsp]
   + Linux [.elf]
   + OSX [.macho]
   + Perl [.pl]
   + PHP
   + Powershell [.ps1]
   + Python [.py]
   + Tomcat [.war]
   + Windows [.exe // .exe-service // .dll]

 Rather than putting <DOMAIN/IP>, you can do a interface and Zacky_PayGen will detect that IP address.
 Missing <DOMAIN/IP> will default to the IP menu.

 Missing <PORT> will default to 443.

 <CMD> is a standard/native command prompt/terminal to interactive with.
 <MSF> is a custom cross platform shell, gaining the full power of Metasploit.
 Missing <CMD/MSF> will default to <MSF> where possible.

 <BIND> opens a port on the target side, and the attacker connects to them. Commonly blocked with ingress firewalls rules on the target.
 <REVERSE> makes the target connect back to the attacker. The attacker needs an open port. Blocked with engress firewalls rules on the target.
 Missing <BIND/REVERSE> will default to <REVERSE>.

 <STAGED> splits the payload into parts, making it smaller but dependent on Metasploit.
 <STAGELESS> is the complete standalone payload. More 'stable' than <STAGED>.
 Missing <STAGED/STAGELESS> will default to <STAGED> where possible.

 <TCP> is the standard method to connecting back. This is the most compatible with TYPES as its RAW. Can be easily detected on IDSs.
 <HTTP> makes the communication appear to be HTTP traffic (unencrypted). Helpful for packet inspection, which limit port access on protocol - e.g. TCP 80.
 <HTTPS> makes the communication appear to be (encrypted) HTTP traffic using as SSL. Helpful for packet inspection, which limit port access on protocol - e.g. TCP 443.
 <FIND_PORT> will attempt every port on the target machine, to find a way out. Useful with stick ingress/engress firewall rules. Will switch to 'allports' based on <TYPE>.
 Missing <TCP/HTTP/HTTPS/FIND_PORT> will default to <TCP>.

 <BATCH> will generate as many combinations as possible: <TYPE>, <CMD + MSF>, <BIND + REVERSE>, <STAGED + STAGELESS> & <TCP + HTTP + HTTPS + FIND_PORT> 
 <LOOP> will just create one of each <TYPE>.

 <VERBOSE> will display more information.
$
```
