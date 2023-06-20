# Setting up new project

1. Setup repo on GitHub with `README.md`, `.gitignore`, `MIT License`.
1. Clone to local machine, `cd` into newly cloned repo, and create and checkout to dev branch 
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

****


## Rough Notes for Starter (using Lab 08)

1. Create a repo (no template, README, MIT License)
1. Add starter code
1. Add all of the configs
1. extract all files from the `api-server` and bring them to the root of the new `auth-api` repo
1. `npm i` AND make sure that all the packages from BOTH package.json files are installed: thses  are the packages that need to be added: `npm i cors bcrypt base-64 
1. How are you going to combine - look at that structure
1. insert `auth` folder (from the `auth-server`) into the new repo's `src` folder
1. make sure adn confirm things work! 
1. models - we need ONE `models/index` so we will ned to import users from `auth/models` into `src/models`




// Propose file structure for Lab09


├── .github
│   ├── workflows
│   │   └── node.yml
├── __tests__
│   ├── auth.test.js (integration test)
│   └── server.test.js
├── src
│   ├── auth
│   │   ├── middleware
│   │   │   ├── acl.js
│   │   │   ├── basic.js
│   │   │   ├── basic.test.js (unit test)
│   │   │   └── bearer.js
│   │   │   ├── bearer.test.js
│   │   ├── models
│   │   │   └── users.js
│   │   └── routes.js
│   ├── error-handlers
│   │   ├── 404.js
│   │   └── 500.js
│   ├── middleware
│   │   └── logger.js
│   ├── models
│   │   ├── blogs
│   │   │   └── model.js
│   │   ├── data-collections.js
│   │   └── index.js
│   ├── routes
│   │   ├── v1.js
│   │   └── v2.js
│   └── server.js
├── .eslintrc.json
├── .gitignore
├── index.js
├── package.json
└── README.md

# auth-api-d53

## My Approach for Task 1:
1. create repo
1. add starter code
1. add all of the configs
1. extract all files from the `api-server`, and bring them to the root of the new `auth-api` repo
1. `npm i` AND make sure that all the packages from BOTH package.json files are installed:  these are the packages that need to be added:  `npm i cors bcrypt base-64 jsonwebtoken` 
1. get proof of life on the `api-server` portion
1. insert `auth` folder (from the `auth-server`) into the new repo's `src` folder
1. make sure all is wired up and confirm things works!
1.  models - we need ONE `models/index.js`, so will need import users from `auth/models` into `src/models` 

## Clear database

Comment this in when you want to clear the DB

```
async function initializeDatabase() {
  try {
    // Synchronize the Regions model with the database table
    await sequelizedDatabase.sync({ force: true });
    console.log('All models were synchronized successfully');
  } catch (error) {
    console.error('Error occurred while syncing all models.', error);
  }
}

initializeDatabase();
```


