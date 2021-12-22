# OneClick Login for Adminer
Display a list of predefined database servers to login with just one click.
Don't use this in production enviroment unless the access is restricted

Create a file servers.php and define your database details with the following structure
```
<?php
return [
	
    '{host}' => array(
		// Required parameters
        'username'  => '{username}',
        'pass'      => '{password}',
        // Optional parameters
        'driver'    => 'pgsql',
        'label'     => 'MySQL',
        'databases' => array(
            '{database_1_name}' => 'Database 1',
            '{database_2_name}' => 'Database 2'
        )
    ),
];
```
Instantiate OnClick Login according to adminer instructions from [adminer](https://www.adminer.org/plugins/#use)
```
new OneClickLogin(include 'path/to/servers.php');
```