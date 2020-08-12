# Deploy-laravel-Project

suppose my site has 

public_html

private

cgi 

////////For Subdomain///////////
eg: you have subdomain = amrit.example.com

You have 2 folder---  1) amrit 2) amrit.example.com


then 

2) clone project inside private/amrit(For Subdomain)

For ex:
   git clone git clone origin-url . 
   
  //Don't forget to use dot at last.(This don't create folder)

3) move public folder contents to public_html/sushil.example.com(for subdomain)
 copy command :- cp -R public ../public_html/
////////////--Not Neccesory--//For some Cases//---//////////////

4) in app.php make debug and development environment

5) move .htaccess to public_html/amrit.example.com(for subdomain)
    -- Move all contents of Public.


6) the  create .env and run composer install/update(if required) and migrations

- make change on public_html/index.php...change direction of autoload.php and app.php
- you must change direction to private/sushil(for sobdomain)
- (../) means one folder out.


7) if i got error 500 so finally changed whole project folders permission -R 755 and storage --> 777 -R

chmod -R 777 storage/ or if not worked hmod -R 777 private/

also chmod 544 public_html/index.php

php artisan key:generate

php artisan passport:install

php artisan passport:keys
