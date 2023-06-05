# Project setup

In the file i will guide you on how to localy run the programs.

## contents
- [Startup order](#startup-order)
    - [DNS](#dns)
    - [State microservice](#state-microservice)
    - [Data microservice](#data-microservice)
    - [Gateway](#gateway) 
## Startup order
----------------
## DNS 
Requirments
- none

To startup the DNS run the following commands:
```cs
# install all packages
$ npm install

# then build and start app
$ npm run start
```

----------------
## State microservice
Requirment
- The DNS is running.
- Have a MongoDB database running with a collection named "dashboards"
- Make sure to add environment variables file (.env) in the root of the project with the following properties:
```cs
# url of the Mongo database
DATABASE_URL="mongodb://localhost:4000/DashBuddy-State"
# port where this app will be accessable
PORT=5000
# url of the DNS
DNS="http://127.0.0.1:3001/register"
```
Then run the following commands:
```cs
# install all packages
$ npm install

# then create build
$ npm run build

# then start app
$ npm run start
```

----------------
### Data microservice

<h2 style="color:red">
    
    Disclaimer! W.I.P, use Seed branch
    
</h2>

Requirments
- The DNS is running
- A Mongo Database with the following url "mongodb://localhost:4001/DashBuddy"

To startup the DNS run the following commands:
```cs
# install all packages
$ npm install

# then fill database
$ npm run seed

# then build and start app
$ npm run start
```

----------------
### Gateway
Requirments
- The DNS is running
- Microservices are running

To startup the gatewat run the following commands:
```cs
# install all packages
$ npm install

# then start app
$ npm run start
```
