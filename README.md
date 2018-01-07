# Useful tools:
SSH Client: [link](http://www.putty.org/)  
Filezilla: [link](https://filezilla-project.org/download.php?type=client)

# Basic Linux Commands:
### man
man : get commands manual.
### cd:
```
cd / : go to root.  
cd /usr/ : got to user folder.  
cd - : goto previous folder.  
cd .. : goto parent folder.    
```

### ls:
```
ls -a : display all.
```

### Managing files: create, copy, move, delete:
```
nano file.txt : create file.txt.
cp file.txt file2.txt : copy file.txt to file2.txt.
mv file2.txt /file.txt : move file2.txt to root folder file.txt.
rm file.txt : remove file.txt from current folder.
```

### Managing folders: create, copy, move, delete:
```
mkdir test : make folder test.
cp -r test/ test2/ : copy folder test and its files.
mv test/ test2/
rm -r test : remove folder.
```

### Managing package:
```
apt-get install package-name : install package-name
apt-get remove package-name : uninstall package-name but keep configuration files.
apt-get purge package-name : uninstall package-name and all it configuration files.
apt-get update : update all packages
apt-get autoremove : delete anciant packages.
```

### restart:
```
reboot
```

### Managing services:
```
service nginx stop : stop service nginx.
service nginx start : start service nginx.
service nginx restart : restart service nginx.
service nginx reload : reload configuration files and settings.
```

### Make executable global:
```
mv composer.phar /usr/local/bin/composer : make composer globally accessible.
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
sudo chown -R www-data permissions/ : assigning right over permissions folder for user www-data.
```  
### Managing firewall:
```
sudo ufw status : check firewall status.
sudo ufw disable
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw enable
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

# Install and test SSL:
Steps to Install SSL: [link](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-16-04)  
Link to test SSL level of securiy: [link](https://www.ssllabs.com/ssltest/)
