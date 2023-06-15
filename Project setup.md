# Project setup

In this file, I will guide you on how to locally run the programs.

## contents
- [Startup order](#startup-order)
    - [DNS](#dns)
    - [State microservice](#state-microservice)
    - [Data microservice](#data-microservice)
    - [Gateway](#gateway) 
## Startup order
----------------
## DNS 
Requirements
- none

To start up the DNS run the following commands:
```sql
# install all packages
$ npm install

# Then build and start the app
$ npm run start
```

----------------
## State microservice
Requirements
- The DNS is running.
- Have a MongoDB database running with a collection named "dashboards"
- Make sure to add environment variables file (.env) in the root of the project with the following properties:
```sql
# url of the Mongo database
DATABASE_URL="mongodb://localhost:4000/DashBuddy-State"
# port where this app will be accessible
PORT=5000
# url of the DNS
DNS="http://127.0.0.1:3001/register"
```
Then run the following commands:
```sql
# install all packages
$ npm install

# then create a build
$ npm run build

# then start the app
$ npm run start
```

----------------
### Data microservice

Requirements
- The DNS is running
- A Mongo Database with the following URL "mongodb://localhost:4001/DashBuddy"

To start up the DNS run the following commands:
```sql
# install all packages
$ npm install

# then fill the database with test data
$ npm run seed

# then build and start the app
$ npm run start
```

----------------
### Gateway
Requirements
- The DNS is running
- Microservices are running

To start up the gateway run the following commands:
```sql
# install all packages
$ npm install

# then start the app
$ npm run start
```
