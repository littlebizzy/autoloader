## Changelog

### 1.2.1
* HOTFIX: `PHP Fatal error: Uncaught TypeError: Return value of LittleBizzy\Autoloader\Autoloader::countPlugins() must be of the type string, integer returned in /var/www/html/wp-content/mu-plugins/autoloader.php:198`

### 1.2.0
* added PHP `strict_types`
* dropped support for PHP 5.x and earlier versions
* various code optimization

### 1.1.0
* tested with PHP 7.0, 7.1, 7.2
* revised code with new PHP namespaces
* changed `wp_options` name to `littlebizzy_autoloader`
* optimized plugin code (e.g. prevent direct calls, minify `wp_options` data, etc)
* improved "duplicate queries" issue: *Effectively when the local plugin option cache is empty (or it is added or removed a mu-plugin directory), there is a double call to the updateCache method that duplicates the query (originated from the pluginsCount method)... There is only one scenario when this double call is made on purpose: the must-use plugins screen, where calls the updatecache method to retrieve all plugins info to show the autoloaded plugins list.*

### 1.0.0
* forked from Roots Bedrock (no functional differences)
* tweaked plugin meta
