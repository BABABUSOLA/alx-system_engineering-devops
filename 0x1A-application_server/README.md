0x1A-application_server

ssh into the server:

task 1:
pip install flask

task 2:
pip install gunicorn

if error is encounterer run:
sudo pip uninstall gunicorn -y
sudo apt-get remove gunicorn --auto-remove -y

sudo pip3 install gunicorn
sudo ln -s "$(which gunicorn)" /usr/bin/gunicorn


Task3:
copy the ngix config file to the server

On the server run: 

add the content of the file 2-app_server-nginx_config and replace with the server object in the 3-redirection file in your server to form 

which i named 2-app_server-nginx-config-full

run: sudo ./2-app_server-nginx-config-full
