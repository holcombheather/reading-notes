# Setting Up

1. Initialize app
   ```node
   npm init -y
   ```
2. Install Dependencies
   ```node
   npm install
   ```
3. Run the following code to initialize the project with the Sequelize config file.
   ```node
   npm run db:init
   ```
4. Modify the `config/config.json` file with your username, database name, and make sure to set the dialect to postgres
   ```json
   {
     "development": {
       "username": "your-username", //Put your username here
       "password": "not-necessary-unless-you-add-this-feature",
       "database": "your-database-name", //Put your db name here (helen_house_database)
       "host": "127.0.0.1",
       "dialect": "postgres" //Defaul mysql, change to postgres
     },
     "test": {
       "username": "root",
       "password": null,
       "database": "database_test",
       "host": "127.0.0.1",
       "dialect": "mysql"
     },
     "production": {
       "username": "root",
       "password": null,
       "database": "database_production",
       "host": "127.0.0.1",
       "dialect": "mysql"
     }
   }
   ```
5. Once you finish editing the config.json file, create the database by running `npm run db:create`

6. Update `.env` file


***
