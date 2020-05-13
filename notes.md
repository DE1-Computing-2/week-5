# SQLITE Lab

## Requirements: a Browser with SQLite Manager extension installed
I use the [Brave browser](https://brave.com/) ofcourse, with [SQLite Manager](https://add0n.com/sqlite-manager.html). You can use FireFox or Chrome too..

## Juppyter notebook set up and running
Please install and run [Jupyter notebook](https://jupyter.org/). We are unable to provide tech support for running this on your machine. Alternatively simply use any Python development environment of your choice.

## Code to run on the Browser/SQLite manager

First, let's create a new Database: call it anything, e.g., `mydatabase.sqlite`

Then, let's declare what goes in it:
`CREATE  TABLE "main"."contributors" ("id" INTEGER PRIMARY KEY  AUTOINCREMENT  NOT NULL , "last_name" VARCHAR, "first_name" VARCHAR, "city" VARCHAR, "state" VARCHAR, "zip" VARCHAR, "amount" INTEGER)`

Now Let's insert some example entries:
`INSERT INTO contributors (last_name, first_name, city, state, zip, amount) VALUES ('Winfrey', 'Oprah', 'Chicago', 'IL', '60601', 500);
INSERT INTO contributors (last_name, first_name, city, state, zip, amount) VALUES ('Chambers', 'Anne Cox', 'Atlanta', 'GA', '30301', 200);
INSERT INTO contributors (last_name, first_name, city, state, zip, amount) VALUES ('Cathy', 'S. Truett', 'Atlanta', 'GA', '30301', 1200);`

Let's inspect the contents a bit:

`SELECT * FROM contributors;`
`SELECT city, state FROM contributors;`


Now let's add somethign that breaks things and see the effect:
`INSERT INTO contributors (last_name, first_name, city, state, zip, amount) VALUES ('Hamed', 'Haddadi', 'London', 'UK', 'SW7', 100);`

And re-inspetc things, or look for unique fields:
`SELECT DISTINCT state FROM contributors;`

`SELECT * from contributors WHERE state='GA';`

Now let's try plotting something:
`SELECT amount FROM contributors | import as myVar`

`plot(myVar, "type=bar")`


Now Download and save the active databse and let's export it.

### You can alternatively download the database here.

## Code to run on the Jupyter notebook

