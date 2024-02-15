
# Initial Project Setup (everything that needs to be done before starting the project)

## 1. Cloning the repository
Find a location on your computer where you want to save the project.
Launch the bash console there and clone the project with the command:
`git clone https://github.com/LazarevicV/od_a_do_s_tri_praseta.git`

## 2. Enter the project
You must be inside the project directory that was just created, with the command:
`cd od_a_do_s_tri_praseta`

## 3. Installing Composer
`composer install`

## 4. Installing NPM
NPM - node package manager, necessary for using the login, registration system, and everything related to users
`npm install`

## 5. Copying the .env file
.env files are usually not stored in the version control system for security reasons. However, there is a .env.example which serves as a template for the .env file needed for the project. Command:
`cp .env.example .env`

## 6. Generating an encryption key for the application
Laravel requires you to have an encryption key for the application which is usually generated randomly and stored in the .env file. Laravel's command-line tools make it easy to generate this key. Run this command in the terminal to generate the key:
`php artisan key:generate`

## 7. Creating an empty database for the application
Create an empty database for your project using the database tools you prefer (any MySQL client can be used, but localhost/phpmyadmin is recommended for a Laravel application).

## 8. In the .env file, add database information so Laravel can connect to the database
Enable Laravel to connect to the database you just created in the previous step. To do this, you need to add the connection details in the .env file.

In the .env file, fill in the values for DB_HOST, DB_PORT, DB_DATABASE, DB_USERNAME, and DB_PASSWORD to match the details of the database you just created. This will allow you to run migrations in the next step.

## 10. Database migration
Once everything is set up according to the steps in the .env file, you can migrate the database. This will create all the tables necessary for the application in your database.
`php artisan migrate`

## 11. Seeding the database
Run the database seeding to enter data into the database.
`php artisan db:seed`

# Running the project on localhost

## 1. Running npm
`npm run dev`

## Running the local development server
To run the local development server, you can run the following command. This will start the development server at http://localhost:8000.
`php artisan serve`
