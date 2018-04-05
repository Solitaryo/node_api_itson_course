### Steps to run this project
> Clone the project: `git clone [project_url]`

> Install dependencies: `npm install`

> Then we need to setup our database, go to section: "Setup Database"

> Now we need to create migrations, so we know that our database configuration is working, so run this command: `npm run migrate`

> Now we can run the project and start with the command: `npm run dev`

### Setup Database ###
#### Install Posgres ###
Mac

`brew install postgres`

Ubuntu

`sudo apt-get install postgres`

Windows

`?... no idea.`

#### Create user, permissions and database for the project.
```bash
psql template1
CREATE USER node_api WITH PASSWORD 'node_api1234!';
CREATE DATABASE node_api_db;
GRANT ALL PRIVILEGES ON DATABASE "node_api_db" TO node_api;
ALTER DATABASE node_api_db OWNER TO node_api;
```

## Extra Info ##

### Init Sequelize
```bash
node_modules/.bin/sequelize init  
```
### Create Model
```bash
node_modules/.bin/sequelize model:generate --name User --attributes firstName:string,lastName:string,email:string
``` 

### Create Seeder
```bash
node_modules/.bin/sequelize seed:generate --name name-seed
```

### To run seeders #
```bash
node_modules/.bin/sequelize db:seed:all
```