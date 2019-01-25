### PROBLEMS
*****

### the uploaded file size exceeds the upload_max_filesize directive in the php.ini

I found lots of confusing information about this. . .<br>
Apparently, there are a lot of php.ini files.  
* I tried editing the `.htaccess` file of the website, (I had to change the permalinks settings to even create the file.  Creating my own didnt work, and now I can't get it to auto generate.)  
* I tried `cd /var/www/mysite/wp-admin/` there is a php.ini file here as well
* I tried `cd /etc/php/7.0/cli` there is also a php.ini file inside

*****

***What Finally Worked*** was 
* `cd /etc/php/7.0/Apache2` 
* `sudo nano php.ini`
* search for the max_upload
* change it to some value higher than the inital 2
*****

### Can't upload theme.  Does the parent directory have priveleges? (or something along these lines)
*****
***what finally worked***
Apache uses `www-data` as the user.  Installing wordpress leaves all files owned by the user, in my case `jakeryan`.  You can't upload files to the server, unless www-data owns the files.  
* `cd /var/www`
* `sudo chown -R www-data mysite`
