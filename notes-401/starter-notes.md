# Setting up new project

1. Setup repo on GitHub with `README.md`, `.gitignore`, `MIT License`.
1. Clone to local machine and create and checkout to dev branch 
    ```node 
    git checkout -b dev
    ```
1. Initialize app 
    ```node
    npm init -y
    ```
1. Install Dependencies   
    ``` node 
    npm install dotenv express jest`
    ```
     or   
    ``` node 
    npm install cors dotenv express eslint jest supertest pg sequelize sequelize-cli sqlite3
    ```
    or
    ``` node 
    npm i base-64 bcrypt cors dotenv express jest pg supertest sequelize sequelize-cli sqlite3
    ```
1. If using _Sequelize_, add the following to the `package.json`
    ```json
    "init:config": "sequelize init:config",
    "db:create": "sequelize db:create"
    ```
1. Run the following code to initialize the project with the Sequelize config file.
    ``` node
    npm run init:config
    ```
1. Modify the `config/config.json` file with your username, database name, and make sure to set the dialect to postgres
    ``` json
    {
      "development": {
        "username": "your-username", //Put your username here
        "password": "not-necessary-unless-you-add-this-feature",
        "database": "your-database-name", //Put your db name here
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
1. Once you finish editing the config.json file, create the database by running `npm run db:create`
1. Copy the configs file from class repo for `node.yml`, `.gitignore`,`.eslintrc.json`. (will not use `eslintrc.json` for REACT). 
    ```node
    cp -r ../seattle-code-javascript-401d53/configs/ .
    ```
