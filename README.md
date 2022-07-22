# apache2-httpd-mod-auth-openidc-okta

##### Okta OpenIDc with Apache mod_auth_openidc Relying Party (RP)

Description: This is a demo project if you want to setup Okta OpenID connect for you sample web application. 

Assumption is you want to add Okta Authentication to your web applciation and your web app is running behind a Apache webserver.


### Okta OpenIDC Setup: 

    Step 1: Setup a Okta developer free account

    Step 2: Create a new web application

    Step 2.1: enter required fields like app name

    Step 2.2: Okta redirect url is a vanity url, so you can configure any app url. For example: if you have an app running "/my-first-website" then you can enter a redirect url like: http://{myhost}:{with_or_without_port}/my-first-website/some-vanity-redirect-url.html 

    a resource doesn't have to exists in the app serving redirect url.

    Step 4: Take note of client id, client secrete, open idc congiguration url.

    Step 5: Create few users in Okta with/without password/reset password/temp password. Okta admin portal will guide you. You can login to your web application using these users.

### localhost setup in your computer

    Step 1: update your computer host file to point localhost to your sample personal domain

    in windows computer: go to system32/drivers/hosts file and add an entry like
    in mac go type in terminal:  sudo nano /etc/hosts

    127.0.0.1   localhost   myfirstwebapp.com
    
    

### Apache setup/app installation

    Step 1: Install and run docker in your local computer

    Step 2: docker pull madhureddy480/apache2-httpd-mod-auth-openidc-okta

    Explained: 

    this docker image has 

    1. Apache server
    
    2. two sample apps installed (both apps are static html pages with some javascript and css)
    
    2.1: App 1: myapp  - accessible at : http://myfirstwebapp.com:8080/myapp
    
    2.2: App 2: html5up-phantom - accessible at : http://myfirstwebapp.com:8080/html5up-phantom
    
    2.3: both apps server same content. I just copy pasted same html pages as two separate apps.
    
    3. mod_auth_openidc module installed.
    
    4. sample configuration properties for you to edit. (exaplined later in this document)
    
    Step 3: run the image with port 8080

    Step 4: login to the container shell 

    Step 5: navigate to conf folder ( cd conf)

    Step 6: execute <command>  cat httpd.conf  </command> if you want to view httpd.conf file 

    Step 7. open httpd.conf file to edit; here you will enter you application's Okta OpenIDc properties. if you can't edit the file, just run <command> chmod 755 httpd.conf </command> to grant write permissions to the file.

    Step 8: restart the docker container, so that your configurations takes effect.

    
   
    
    
    
    
    
    
    
    



