# how-to-create-wordpress-on-azure

HOW TO CREATE A WORDPRESS SITE ON AZURE APP SERVICE LINUX
1.	create app service: using php as the base 
2.	create MySQL server. 
3.	use ssh to deploy following this commands:
a.	cd site/wwwroot/ : this changes directory to where we should be
b.	wget -c http://wordpress.org/latest.tar.gz : used to download the latest version of wordpress
c.	tar -xzvf latest.tar.gz : unzip the version
d.	mv wordpress/* /home/site/wwwroot/ : moves the downloaded and unzipped wordpress to where it shoould be
e.	rm -r latest.tar.gz   and    rm -rf wordpress/   removes the wordpress file
4.	Then navigate to the app url in the azure portal
5.	uname:ekunkoya
6.	URL: http://olek-webapp-test.azurewebsites.net/wp-admin/
Configure SQL connection using workbench
1.	Enter preferred connection name
2.	Enter hostname. This equals to the SQL server name
3.	Enter username. This equals the server admin login name
4.	Enter the password used while configuring the SQL server. It can be reset if forgotten. Click on connect
5.	Add the IP of the machine which you are connecting it. Go to connection security and click on Add client IP then enter the IP of the machine.
6.	Click connect and then click on schemas which will open sys
7.	Create a new database for the wordpress site. Right click on sys in the workbench and click on create schema. Enter the name for the database
Configure Wordpress
1.	Enter the just created database name
2.	For username enter the SQL server admin login name
3.	Password is the one used while configuring the dbase
4.	Database host is the server name
5.	Go to sql server settings and disable the enforce SSL connection and enable allow access to azure services
Configure SSL
1.	
YouTube video: 
Hosting WordPress on Azure: https://www.youtube.com/watch?v=api6HM4kpWc
WordPress Tutorial: https://www.youtube.com/watch?v=6gosrWrGF9Q
•	Change permalink: dashboard-settings-permalink
•	Delete all plugins
•	Install: yeost seo, w3 total cache, lite speed cache
•	Change title and tagline: Customize-site identity
•	Create theme: use astra
•	Install starter template plugin
o	Plugins – add new – search for ‘starter templates’ – add astra starter templates – appearance – starter templates – choose elementor 
•	Change Theme Style – edit with elementor – menu – theme style
o	Typography – 
•	Add and delete pages: dashboard – pages -add new – enter title – edit with elementor
•	Add Navigation: customize – menu – navigation – add -items  
o	Change menu link color: header – transparent header – 
•	Logo design: customize – header – site identity – change logo 
o	Logo to the right then text
o	Use photopea.com to create your logo. It is a free photoshop clone.
o	Use iconfinder.com to search for icons
o	 Download from photopea as png
