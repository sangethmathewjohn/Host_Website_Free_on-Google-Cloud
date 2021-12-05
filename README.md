# Host_Website_Free_on-Google-Cloud

## Install apache on Cloud Console

    sudo apt install apache2
    sudo /etc/init.d/apache2 start
    sudo /etc/init.d/apache2 status
    
## Install Ngrok on the Cloud Console

    sudo curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null &&
              echo "deb https://ngrok-agent.s3.amazonaws.com buster main" | sudo tee /etc/apt/sources.list.d/ngrok.list &&
              sudo apt update && sudo apt install ngrok   
    
## Setup Ngrok

    ngrok authtoken <token>
    
Token will be available to you when you get login into the ngrok.

    ngrok http <port>
    
Now you will get the link that is open to the public in ngrok console.
Whn you get into it apache default page will be loaded into you brower.
              
## Setup your Page.

To load your page change the content in index.html in apache

    sudo cd /var/www/html
    ls

Now you will get the index.html 
Repalce the index page with your own content 
Or you can change the path in default.conf

    sudo cd /etc/apache2/sites-available
    sudo nano default.conf
    
Change the path where the path will  [var/www/html]

## Restart Apache server.

    sudo /etc/init.d/apache2 restart
    sudo /etc/init.d/apache2 status
  
The command may vary depending upon the file name..
