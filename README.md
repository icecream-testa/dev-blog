**Install Module**

To install this module via composer you need to execute the following commands in you root directory:

```
composer config repositories.testa github https://github.com/icecream-testa/dev-blog.git
composer require icecream-testa/dev-blog:dev-master
bin/magento setup:upgrade
```

**How to use**

Visit your local project and add the following URL-Key to the base URL:
```
/devblog
```
Enjoy the view! 

**Uninstall Module**

Run command:
```
bin/magento module:disable Testa_Blog  
```
To clean up the database, run the following queries on your database:
```
DELETE FROM setup_module WHERE module = 'Testa_Blog'; 
DELETE FROM cms_page WHERE identifier = 'devblog'; 
DELETE FROM url_rewrite WHERE request_path = 'devblog'"
```
