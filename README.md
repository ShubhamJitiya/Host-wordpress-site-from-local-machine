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
	
	
