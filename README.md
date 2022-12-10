Node JS Job Portal Backend Project
This is a NodeJS powered Web Application, Backend and API Resource hub for it's client interface.

Installation
Prepare a location for the project. We will name the directory job_portal. Inside the project directory, set up git and pull from the repository. Or alternatively, download the project to the location.

git init
git pull https://github.com/saibairi/Job_Hiring_App.git
OR

git clone https://github.com/saibairi/Job_Hiring_App.git .
Install dependencies. This may take a while.

npm install
Create a .env file at the project root and copy contents from here into it.

HOST=localhost
PORT=3000
NODE_ENV=development

APP_NAME=job_portal

DEV_DB_HOSTNAME=localhost
DEV_DB_NAME=Hiring_DB
DEV_DB_USERNAME=
DEV_DB_PASSWORD=

TEST_DB_HOSTNAME=localhost
TEST_DB_NAME=Hiring_D
TEST_DB_USERNAME=
TEST_DB_PASSWORD=

PROD_DB_HOSTNAME=localhost
PROD_DB_NAME=Hiring_D
PROD_DB_USERNAME=
PROD_DB_PASSWORD=

JWT_SECRET=<YOUR JWT SECRET HERE>
JWT_LIFESPAN=600
Generating a secure JWT Secret

In the console run the following commands:

node
require('crypto').randomBytes(64).toString('hex')
OR simply call the package.json script that has been set up to quickly generate a cryptographically secure string

npm run crypto
Copy the cryptographically secure string and use it as your JWT_SECRET

When you have set up your database configuration, the following scripts can be used to quickly setup the server.

Run server using nodemon

npm run server
Todo
Create Login and Registration system
Create Authentication and Authorization system
Create Crud Operations with validations
Unit tests
