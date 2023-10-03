0x0F-load_balancer

Task 0. Double the number of webservers:

Ssh into the server: ssh 'ubuntu@54.210.194.248' 
Add public ssh to server: ssh-copy-id -f -i key.pub ubuntu@54.210.194.248 
copy one file using bash script to server: sudo ../0x0C-web_server/0-transfer_file ../0x0C-web_server/3-redirection 54.210.194.248 ubuntu ~/.ssh/id_rsa(cleared the duplicate error i was having after removing the default file in the etc folder and running 3-redirection again using sudo
sudo ../0x0C-web_server/0-transfer_file 0-custom_http_response_header 54.210.194.248 ubuntu ~/.ssh/id_rsa
Then after ssh into the server, run : sudo ./3-redirection and sudo ./0-custom_http_response_header

Open another tab simultaneously and Repeat above also for the second server 100.25.130.22
