# README

Sample blog application to meet the needs of the CloudFoundry deployment.

## Authentication

Username: `admin`

Password: `password`

## Pre-requisites for running the application
  * You will require the pg_config binary, which will usually be included with a postgres package. The libpq-dev package will also be required on Debian machines.
  * You will require ruby v2.3.0 or higher.
  * You will require bundler:
```
gem install bundler
```

## Installation

Installation is really simple. First, we'd like to install any dependencies required by the blog.

```
bundle install
```

Be patient, it may take a short while to complete.

This application uses the database. You may want to set up your connection in `config/database.yml`. 
You may also proceed which will cause usage of `sqlite3` driver.

**Fun fact time**

Thanks to the magic of Rails, we can also use `ENV` variables, to configure our connection with the database.
Simply by setting the `DATABASE_URL` variable, we can force the application to attempt the connection 
to provided database.

Once the bundle has gathered all required packages and the database has been set, 
you may want to run the database migration script.

```
rake db:migrate
```

Great! This should prepare your database for the new experience of this application.

Run the application, by executing the following command.

```
bin/rails server
```

All done! Read the output provided by the application. 
It will mention URL your application can be accessed from and maybe some other potentially useful information. 

Enjoy your new, very simple, blog application!
