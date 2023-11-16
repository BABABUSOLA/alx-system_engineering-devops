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
