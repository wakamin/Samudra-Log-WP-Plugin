# Samudra-Log-WP-Plugin
Write log for debugging Wordpress site.

## How to Use?
Use this function to write log.
```php
// Variable value can be string, array, or object
$variable = 'Variable value';

// Log file will be in /wp-content/plugins/samudra-log/log/sd_log.log
sd_log($variable);

// Log file will be in /wp-content/plugins/samudra-log/log/my-file.log
sd_log($variable, 'my-file');
```

## Restrict direct access to log file
If you are using Nginx, put this code inside your server block.
```nginx
location ~ /wp-content/plugins/samudra-log/log/.*\.log$ {
    deny all;
    return 404;
}
```
