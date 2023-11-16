0x1A-application_server

ssh into the server:

task 0:
pip install flask

task 1:
pip install gunicorn

if error is encounterer run:
sudo pip uninstall gunicorn -y
sudo apt-get remove gunicorn --auto-remove -y

sudo pip3 install gunicorn
sudo ln -s "$(which gunicorn)" /usr/bin/gunicorn


Task 2:
copy the  respective ngix config file to the server

On the server run: 

sudo cp 2-app_server-nginx_config /etc/nginx/sites-available/default
sudo cp 2-app_server-nginx_config /etc/nginx/sites-enabled/default
sudo service nginx restart

Task 3:
copy the  respective ngix config file to the server

On the server run:

sudo cp 3-app_server-nginx_config /etc/nginx/sites-available/default
sudo cp 3-app_server-nginx_config /etc/nginx/sites-enabled/default
sudo service nginx restart
