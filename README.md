# Prepare for Ubuntu Server Setup
```shell
cd
git clone https://github.com/FierceBengalTiger/ubuntu-server-setup-script.git
cd ubuntu-server-setup-script
chmod +x install.sh
sudo ./install.sh
```
- > It will create and configure your server.
- > Just you need to add the vhost conf files as per your requirements.
 *[We include the sample conf files]*
- > Just you need to configure your Jenkins configuration. 
- > Lastly it also install the mysql secure installation script so you need to configure your DB settings.

# Add conf for your Domain
```shell
sudo cp /server-setup-script/sample_conf /etc/nginx/sites-available/example.com.conf
sudo ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/example.com.conf
sudo vim /etc/nginx/sites-available/example.com.conf
```

# Add conf with SSL for your Domain
```shell
sudo cp /server-setup-script/sample_ssl_conf /etc/nginx/sites-available/example.com.conf
sudo ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/example.com.conf
sudo vim /etc/nginx/sites-available/example.com.conf
```

- > Change `example.com.conf` as per yours.
- > Find `# Modify - ....` on conf file and change as per yours.

# Restart Nginx server

```shell
sudo systemctl restart nginx
```

# Know Nginx status

```shell
sudo systemctl status nginx 
```

# Get First Password for Jenkins and Configure for Project
```shell
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Special thanks to [Behestee](https://github.com/behestee/awssh/) bhaiya.


