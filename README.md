# Host-wordpress-site-from-local-machine
How to upload wordpress site from local host to live server with all errors resolved

1. Create zip of wordpress

2. Download unzipper : https://github.com/ndeet/unzipper

3. Upload both (wordpress.Zip + unzipper) to file manager of hosting provider

4. Use filezilla to perform step 3
	- Download client file : https://filezilla-project.org/
	- Enter host name, username, port, pass [this maybe diff than useracc]
	- After establishing connection: drag-drop files from local to server 		[LHS TO RHS]

5. Once both file uploaded, extract wordpress.zip by unzipper
	- write in url (browser - in file manager of server) ../unzipper
	- Click on unzip archive
	- move all wordpress files to root file [public html]
	
6. Now set up database
	- Create db name, user name, password
	- export db from local machine 
	- [ in case facing issue while exporting download 5.3+ of php admin and replace all file of PHPMyAdmin : https://www.phpmyadmin.net/downloads/]
	- https://www.youtube.com/watch?v=yEWlyAjKH6M&list=LL&index=1
7. Update public_html
	- Update dbname, dbusername, pass as per point 6 in 'wp-config.php' under file manager/public html
	- 
8. Edit exported .sql file
	- Update url [http://localhost:9090/dir1/dir2...] to your url/domain 
		TO 	ALL 	PLACES
	- Update dbname, dbusername, pass as per point 6. [Must check pass not as 		per profile sometimes]
	- ERROR mysqli_real_connect() local host now allowed: 
		- open mysql.ini 
		- write skip-grant-tables above port = XXXX;
		[https://www.youtube.com/watch?v=vzs9Z12OTE4&list=LL&index=2&t=130s]

9. Import to databaseManager > phpAdmin
	- Inside under your dbname refer point 6

10. Unable to publish or access pages?
	- Check whether all 'localhost' is replaced with your url?
	- Update permalink to post

11. ALL DONE ENJOY YOUR SITE

Videos to refer:
1.  [Complete setup - 000wedhost](https://youtu.be/vVqlYHdQHP4)
2. [Complete setup - General](https://youtu.be/E_3ljmegi9Q)
3. [Publishing failed](https://youtu.be/dkSgTEGUq-o)
4. [Ftp_put(): Can’t open that file](https://youtu.be/NBvg6JJtzDo)
5. [Network error when i exporting](https://youtu.be/yEWlyAjKH6M)
6. [mysqli_real_connect(): (HY000/1130)](https://youtu.be/vzs9Z12OTE4)
7. [FileZilla to Connect FTP](https://youtu.be/pA_ORnPMeL4)

Spent almost more than 16+ hour in solving errors🥲
Here is the notes to never forget again😎🌝
	
