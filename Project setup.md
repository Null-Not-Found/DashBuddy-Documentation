# Project setup

In this file, I will guide you on how to locally run the programs.

## Contents

- [Startup order](#startup-order)
- [Front-end](#front-end)
- [DNS](#dns)
- [State microservice](#state-microservice)
- [Data microservice](#data-microservice)
- [Gateway](#gateway)
***

## Startup Order

To set up and run the project locally, you need to follow the startup order mentioned in the guide. Here's the recommended order to start up the different components:

    - DNS
    - State microservice
    - Data microservice
    - Gateway

The Front-end doesnt rely on other components to start, but it needs all other services to function.

## Front-end

Requirements
- none

To start up the front-end run the following commands:
```sql
# install all packages
$ npm install

# Then build and start the app
$ npm run build
```
***

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
## Data microservice

Requirements
- The DNS is running
- A Mongo Database
- Create .env file in the root folder and add there DATABASE_URL(MongoDB) and PORT (app going to listen this port)

To start up the DNS run the following commands:
```sql
# install all packages
$ npm install

# then fill the database with test data
$ npm run seed
# after 5-10 sec press CTRL+C to Determinate process

# then build
$ npm run build
    
# start the app
$ npm run start
```

----------------
## Gateway
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
