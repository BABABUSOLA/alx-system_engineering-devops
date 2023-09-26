0x0C-web_server

Task 1-install_nginx_web_server steps:

Ssh into the server: ssh 'ubuntu@54.210.194.248'
Add public ssh to server: ssh-copy-id -f -i key.pub ubuntu@54.210.194.248
copy one file using bash script to server: sudo ./0-transfer_file 1-install_nginx_web_server 54.210.194.248 ubuntu ~/.ssh/id_rsa
Then run : sudo ./1-install_nginx_web_server

Task 2-

Domain setup guide: https://docs.google.com/document/d/1QIjkJMmrOy5k7KHs4ztnFx-fBXPpxxJ4yZpxi5JSk4s/edit

Task 3: 

Follow step 1 ,
then run: sudo ./3-redirection
