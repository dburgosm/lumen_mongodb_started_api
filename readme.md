#Lumen + MongoDB 

- Lumen (5.2.6) (Laravel Components 5.2.*)
- https://github.com/jenssegers/laravel-mongodb
- https://github.com/sohelamin/lumen-route-list
- https://secure.php.net/manual/en/mongodb.installation.php


#Configure Virtual Host Apache:

```html
<VirtualHost *:80>
  ServerName lumen.localhost.app
  DocumentRoot "your_path/public"
  <Directory "yout_path/public">
    AllowOverride all
  </Directory>
  ErrorLog "/var/log/apache2/lumen-error_log"
  CustomLog "/var/log/apache2/lumen-access_log" common
</VirtualHost>
```
#Example:
- Lumen version:
```sh
http://lument.localhost.app/
```
- Run: 
```sh
php artisan db:seed to create new user
```

- Show new user created: 
```sh
http://lument.localhost.app/user
```
- JSON response:
```json

	{
		"success":true,
		"code":200,
		"message":"All is ok :)",
		"data":[{
			"_id":"56f6edc525a53beb656ef9f1",
			"name":"David Burgos M",
			"email":"dburgosm@gmail.com"
		}]
	}
```
