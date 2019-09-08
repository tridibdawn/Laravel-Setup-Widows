# Laravel-Setup-Widows
This repository contains info about how to setup laravel in windows
# Install Laravel in htdocs
```
laravel new myApp
```
# Setup v-host to access your laravel via a simplified url
> Goto c:\xampp\apache\conf\extra\httpd-vhosts.conf
# Add the following to the bottom
```
<VirtualHost *:80>
    DocumentRoot "C:/xampp/htdocs"
    ServerName localhost
</VirtualHost>

<VirtualHost *:80>
    DocumentRoot "C:/xampp/htdocs/laravel-test/public"
    ServerName laratest.test
</VirtualHost>
```
# Add the url of your application to 127.0.0.1
> Open notepad or any other text editor as administrator
> Go to C:\Windows\System32\drivers\etc and open "hosts" file
# Add the following lines to the bottom
```
127.0.0.1 localhost
127.0.0.1 laratest.test
```
> Save and close the "hosts" file and Restart your apache server

> Now visit your URL in your browser "laratest.dev"
