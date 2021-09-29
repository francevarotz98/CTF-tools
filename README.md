# CTF-tools
Collection of useful tools for CTFs.


## Categories
  - [Web](#web)
  - [Crypto](#crypto)
  - [Steganography](#stego)
  - [Binary](#binary)
  - [Other](#other)
  - [Useful](#useful)
  - [to update]

---

## Web

* nmap
```
Example usage : sudo nmap -sS -A -T4 <ip_target> -oN <name_output> -vv
```
* gobuster
```
Example usage for directory/file enum :
                gobuster dir -u <ip_target> --wordlist <path_to_wordlist> -x <extensions>
  where:  * path_to_wordlist can be something like "/usr/share/wordlists/<wordlist>"
          * extensions like php, txt, js, cgi, sh, ...
```
* dirb
* curl
* nikto
```
Example usage: nikto -h <ip_target>
```
* wpscan
* wget 
```
Example usage: wget <url>
```

---

## Crypto

* [CyberChef](https://gchq.github.io/CyberChef/)

---

## Steganography

* steghide
```
Example usage: steghide <command> <file>
  where command can be:   > info
                          > extract 
                          > embed 
```
* [Stegosolve](http://www.caesum.com/handbook/Stegsolve.jar)

---

## Binary

* checksec
* strings
* ltrace
* strace
* apktool
* frida
* gdb / gdb-peda

---

## Other

* nc -- TCP/IP swiss army knife
* linpeas.sh -- for Linux Privesc
* sudo -l -- to get which files I can run with sudo
* searchsploit -- search through Exploit db archive
```
Example usage: searchsploit OpenSSH 7.2p2
               searchsploit -p 46635  -- it returns the URL of the CVE in exploit db
```
* msfconsole -- the god tool for exploitation


---



## Useful

* sending a file using nc:
```
client side : nc -lvp <port> > <file>
server side : nc <ip_server> <port_server> < <file>
```
* sending a file using nc + wget:
```
client side : nc -lvp <port> < <file>
server side : wget <ip_server>:<port_server>/<file>

!! [NOTE: protocol will continue after transmission of file (maybe because client side does not receive CRLF sequence). So after a while, just press CTRL+c et voit-là] 
```
* to convert a python script from v.2 to v.3
```
python3 -m lib2to3 <script>.py -w
```
* connect to server pop3 (port 110) using telnet:
```
    telnet <ip> 110
```


---




# Contributors

- Francesco Varotto - [@frarotto](https://github.com/francevarotz98/)
- Massimiliano Belluomini - [@massibelluomini](https://github.com/massibelluomini)
