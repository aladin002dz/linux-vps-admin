# Example Of installing a VPS with LEMP stack on [DigitlOcean](https://www.digitalocean.com/)
1. Using DigitalOcean, Choose the LEMP image.
1. Link the domain name to the VPS IP ADDRESS.
1. Connect to the Server with SSH, on windows: [putty](http://www.putty.org/) / on mcOS: ssh command.
1. Update package and reboot
    ```
    apt-get update
    apt-get upgrade
    reboot #restart server
    ```
1. Secure mysql database:
```
sudo mysql_secure_installation
```
  then basically yes for every question.
1. Configuring nginx
  *. Configuration /etc/nginx
  *. Website Files: /var/www
  
# Useful tools:
SSH Client: [link](http://www.putty.org/)  
Filezilla: [link](https://filezilla-project.org/download.php?type=client)

# Basic Linux Commands:

### man
```
man # get commands manual.  
```  

### pwd  
```
pwd # path of the current directory.  
```

### cd:  
```
cd /      # go to root.  
cd /usr/  # got to user folder.  
cd -      # goto previous folder.  
cd ..     # goto parent folder.    
```

### ls:
```
ls -a # display all.
```

### Managing files: create, copy, move, delete:
```
nano file.txt          # create file.txt.
cp file.txt file2.txt  # copy file.txt to file2.txt.
mv file2.txt /file.txt # move file2.txt to root folder file.txt.
rm file.txt            # remove file.txt from current folder.
```

### Managing folders: create, copy, move, delete:
```
mkdir test         # make folder test.
cp -r test/ test2/ # copy folder test and its files.
mv test/ test2/
rm -r test         # remove folder.
rmdir test         # remove empty folder.
rm -ri test        # add confirmation to remove folder.
```

### Managing package:
```
apt-get install package-name # install package-name
apt-get remove package-name  # uninstall package-name but keep configuration files.
apt-get purge package-name   # uninstall package-name and all it configuration files.
apt-get update               # update all packages
apt-get autoremove           # delete anciant packages.
```

### restart:
```
reboot
```

### Managing services:
```
sudo service docker status # check status of service docker
service nginx stop    # stop service nginx.
service nginx start   # start service nginx.
service nginx restart # restart service nginx.
service nginx reload  # reload configuration files and settings.
```

### Make executable global:
```
mv composer.phar /usr/local/bin/composer # make composer globally accessible.
```

### Generate ssh key:
```
ssh-keygen -t rsa -b 4096 -C "root"
```

### Add user:
```
adduser test
```

### Remove user:
```
deluser test
rm -r /home/test
```  
### Add admin rights to user:
```
sudo adduser user_test sudo
```  
### Assigning permissions for user over a folder:
```
sudo chown -R www-data permissions/ # assigning right over permissions folder for user www-data.
```  

### Manage File and Folder Permissions 

Who are we changing the permission for? [ugoa] - user (or owner), group, others, all
Are we granting or revoking the permission - indicated with either a plus ( + ) or minus ( - )
Which permission are we setting? - read ( r ), write ( w ) or execute ( x )

```
chmod [permissions] [path]
```

Using Binary References to Set permissions: The first number represents the Owner permission; the second represents the Group permissions; and the last number represents the permissions for all other users. The numbers are a binary representation of the rwx string.

```
chmod 740 file1
```

### Managing firewall:
```
sudo ufw status                  # check firewall status.
sudo apt-get install ufw         #if not installed
sudo ufw enable                  #activate the firewall
sudo ufw disable
sudo ufw default deny incoming   # deny incoming connections
sudo ufw default allow outgoing  # deny outgoing connections
sudo ufw allow ssh
sudo ufw allow www               #allow port 80 (http)
sudo ufw allow 443/tcp           #allow manually port 443 (https)
sudo ufw delete allow 80/tcp          #deny access with http
```  
### Configuration file for nginx:
/etc/nginx/nginx.conf  
### Websites Folder:
/var/www/  
# Secure mysql database:
```
sudo mysql_secure_installation
```  
then basically yes for every question.

### Configuration file for nginx:
/etc/nginx/nginx.conf

### Websites Folder:
/var/www/

# Install and test SSL:
Steps to Install SSL: [link](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-16-04)  
Link to test SSL level of security: [link](https://www.ssllabs.com/ssltest/)


