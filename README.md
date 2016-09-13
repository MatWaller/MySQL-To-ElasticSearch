<h1>MySql2Elastic</h1>

<h2>Description</h2>
A OpenSource Web application for migrating Simple Mysql Tables and their Data into Elasticsearch using the PHP Elastica Libary this is a ongoing project as development progresses the ability to migrate more complex tables will be added.<br><br>

Mysql2Elastic gives you the ability to migrate all tables or selected tables from a MySql Database and convert them to ElasticSearch Index(s) it is very simple to use using either the command line application or the simple Web interface.<br><br>

Migrations can be done using a live database (Local or Remote) or by providing a SQL file.<br>

Simply put this is a set of tools for migrating MySql to ElasticSearch

<h2>Issues and Pull Requests.
As Development is on going some tables may not be migrated correctly to assist with development i would appreciate if you could raise a issue on GitHub, Pull requests will be happily accepted if they are of good quality and improve functionality or fix bugs/issues.<br>


<h2>Set up</h2>
Simply clone the repository on either your local machine or server; <br>
```git clone https://github.com/wallermadev/MySQL-To-ElasticSearch.git```

Enter the cloned directory;<br>
```cd MySQL-To-ElasticSearch.git```

install the dependancies using composer;<br>
```php composer.phar install```

Edit configuration to use your ElasticSearch Installation (Skip this step if you are using the web interface);<br>
```nano config/Elastic.conf```

Update IP, Port and login credentials (if Applicable) To that of your ElasticSearch Instance this step is only needed if you intend to use MySql2Elastic using the command line interface as a configuration file will be generated if you are using the web interface.<br><br>


Edit configuration to use your Mysql Installation (Skip this step if you are using the web interface);<br>
```nano config/Mysql.conf```

Update IP, Port and login credentials (if Applicable) To that of your MySql Server this step is only needed if you intend to use MySql2Elastic using the command line interface as a configuration file will be generated if you are using the web interface.<br><br>

Additional configuration such as memory limit, maximum execution time, Error logging options etc... can be set inside;<br>
```nano config/extra.conf```



<h2>Usage Command Line</h2>

<h2>Usage Web Interface</h2>
If you are using the Web interface run the shell script startServer.sh using the command;<br>
```bash startServer.sh```

You can use screen to run the server in the background using;<br>
```screen ./startServer.sh```

If the server successfully started you can access it via your web browser on port 4321 for example if you are running the server on your local machine you can access the web interface by visiting;<br>
```link-: http://127.0.0.1:4321```

From here follow the on screen instructions to configure the the credentials for the target ElasticSearch Installation and Host Mysql Installation after the initial configuration you are able to set Additional options and Edit the ElasticSearch/Mysql Configuration by accessing the "Configuration" In the main menu. <br><br>

If you have configured everything correctly the status in either the status widget or on the status page will display GREEN with the message "Everything Connected fine" the status feature works by polling the server and logging in -- if there is a error while doing do The status will display RED with a message regarding what went wrong, there are also warning statuses which are yellow these are rare and are usually related to a slow connection/reply to the host or target servers you can continue with error but do so at your own risk!<br><br>

If everything went well and your status is not showing any errors you will be redirected to a page to select the database on the MySql host when selected a select box will be displayed with all possible tables that can be migrated you can select any amount <em>however for best result only migrate between 1-5 at a time.</em></br></br>

After the database has been selected and you have chosen the tables you want to migrate click the Migrate Button A modal will appear and show migration progress if any as it progresses the "Log Box" will update showing Progress/Errors/Warnings.<br><br>

Congratulations! If all went well you will have successfully migrated your Mysql Database/Tables and data to ElasticSearch!<br><br>
If a unexpected error occured please check the "Common Problems" Section for a solution if a solution can not be found please submit a Issue and i will try assist you the best i can.
</h3>Additional Information</h3>
