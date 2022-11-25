### To install NGINX server

`sudo apt install nginx`

### Location of conf file

`/etc/nginx/sites-available`

### To edit the default conf file

`sudo gedit /etc/nginx/sites-available/default`

### To start NGINX server

`sudo systemctl start nginx`

### To stop NGINX server

`sudo systemctl stop nginx`

### To check validity of NGINX conf

`sudo nginx -t`

### To reload NGINX server

`sudo systemctl reload nginx`

### To restart NGINX server

`sudo systemctl restart nginx`

### To check NGIINX process status

`sudo systemctl status nginx`
