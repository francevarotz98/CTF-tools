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

* toadd

---

## Steganography

* steghide
```
Example usage: steghide <command> <file>
  where command can be:   > info
                          > extract 
                          > embed 
```

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


---



## Useful

* sending a file using nc:
```
server side : nc -lvp <port> > <file>
client side : nc <ip_server> <port_server> < <file>
```
* sending a file using nc + wget:
```
server side : nc -lvp <port> < <file>
client side : wget <ip_server>:<port_server>/<file>

!! [NOTE: protocol will continue after transmission of file (maybe because client side does not receive CRLF sequence. So after a few time, just press CTRL+c et voit-là] 
```

---




# Contributors

- Francesco Varotto - [@frarotto](https://github.com/francevarotz98/)
-  toadd
