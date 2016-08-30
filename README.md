# README

Sample blog application to meet the needs of the CloudFoundry deployment.

## Authentication

Username: `admin`

Password: `password`

## Installation

Installation is really simple. First, we'd like to install any dependencies required by the blog.

```
bundle install
```

Be patient, it may take a short while to complete.

This application uses the database. You may want to set up your connection in `config/database.yml`. 
You may also proceed which will cause usage of `sqlite3` driver.

Once the bundle has gathered all required packages and the database has been set uo, 
you may want to run the database migration script.

```
rake db:migrate
```

Great! This should prepare your database for the new experience of this application.

Run the application, by executing the following command.

```
bin/rails server
```

All done! Enjoy your new, very simple, blog application!