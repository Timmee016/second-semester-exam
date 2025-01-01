# second-semester-exam
this is a repository containing details of uploading my html page to a web server
first i create an instance with its ssh key pair
while creating this instance, i ensure that my http with port 80 and ssh with port 22 i enabled
then i download nginx web server using command 'sudo apt install nginx -y'
then i start and enable web server using command 'sudo systemctl start nginx and sudo systemctl enable nginx'
i create my html landing page and upload by creating a directory using command "sudo mkdir -p /var/www/timmees-skincare.com"
and copy my html file i.e teams.html to directory 
then I uploaded the file to the directory via my local machine using scp command, "scp -i ~/.ssh/seconsem.pem team.html ubuntu@your-server-ip:/var/www/timmees-skincare.com/"
Then I created my nginx configuration file for the site using "/etc/nginx/sites-available/timmees-skincare.com" 
Then I tested my configuration and enabled it using commands,
"sudo ln -s /etc/nginx/sites-available/timmees-skincare.com /etc/nginx/sites-enabled/,sudo nginx -t,sudo systemctl reload nginx"
and I ensured my permissions were set for nginx to be able to read my file using commands,"sudo chown -R www-data:www-data /var/www/timmees-skincare.com
sudo chmod -R 755 /var/www/timmees-skincare.com"
after I was done I updated my 
