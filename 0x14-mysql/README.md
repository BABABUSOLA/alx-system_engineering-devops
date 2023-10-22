0x14-mysql

Task 0:

SSH into server 1 and server 2 separately for each do the step below

[How to] Install mysql 5.7
Copy the key here to your clipboard

https://dev.mysql.com/doc/refman/5.7/en/checking-gpg-signature.html

Save it in a file on your machine i.e. signature.key and then

sudo apt-key add signature.key
add the apt repo

sudo sh -c 'echo "deb http://repo.mysql.com/apt/ubuntu bionic mysql-5.7" >> /etc/apt/sources.list.d/mysql.list'
update apt

sudo apt-get update
now check your available versions:

vagrant@ubuntu-focal:/vagrant$ sudo apt-cache policy mysql-server
mysql-server:
  Installed: (none)
  Candidate: 8.0.27-0ubuntu0.20.04.1
  Version table:
     8.0.27-0ubuntu0.20.04.1 500
        500 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 Packages
        500 http://security.ubuntu.com/ubuntu focal-security/main amd64 Packages
     8.0.19-0ubuntu5 500
        500 http://archive.ubuntu.com/ubuntu focal/main amd64 Packages
     5.7.37-1ubuntu18.04 500
        500 http://repo.mysql.com/apt/ubuntu bionic/mysql-5.7 amd64 Packages
Now install mysql 5.7

sudo apt install -f mysql-client=5.7* mysql-community-server=5.7* mysql-server=5.7*


TASK 1

To achieve this, you'll need to log in to each MySQL server (`web-01` and `web-02`) and perform the necessary steps. Here's a step-by-step guide:

1. **Access MySQL on web-01**:

   ```bash
   mysql -u root -p
   ```

   You will be prompted for the MySQL root password.

2. **Create the user**:

   ```sql
   CREATE USER 'holberton_user'@'localhost' IDENTIFIED BY 'projectcorrection280hbtn';
   ```

   This command creates the user `holberton_user` with the specified password and allows them to connect only from the `localhost`.

3. **Grant necessary privileges**:

   To allow `holberton_user` to check replication status, you need to grant the `REPLICATION CLIENT` privilege:

   ```sql
   GRANT REPLICATION CLIENT ON *.* TO 'holberton_user'@'localhost';
   ```

   Additionally, if you want to allow `holberton_user` to view status, you can grant the `SHOW DATABASES` privilege:

   ```sql
   GRANT SHOW DATABASES ON *.* TO 'holberton_user'@'localhost';
   ```

4. **Flush privileges**:

   After making changes, you need to reload the privileges for them to take effect:

   ```sql
   FLUSH PRIVILEGES;
   ```

5. **Repeat the above steps on web-02**:

   Log in to `web-02`, access MySQL, and repeat the same steps to create the `holberton_user` with the specified details and grant necessary privileges.

Now, `holberton_user` should be able to check the replication status on both `web-01` and `web-02` servers.

Please remember to replace `your_password_here` with the actual password you want to use. Always consider the security implications of creating new users and granting privileges. Make sure to follow best practices for user management.

TASK 2:
