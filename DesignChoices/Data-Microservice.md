# Data-Microservice design choices

## Language and Frameworks
### Nest.js, TypeScript, GraphQL.
Nest.js: it has built-in support for GraphQL and is well-suited for building GraphQL APIs. Nest.js provides an easy and convenient way to define GraphQL schemas and resolvers, and it offers several features that can help developers to build scalable and maintainable GraphQL APIs.
TypeScript: with its static typing capabilities, aids in catching errors during development and improves code maintainability. The ability to define types and interfaces enhances code readability and promotes seamless collaboration within teams.
GrapQL: One of the key advantages of GraphQL is its ability to empower clients by allowing them to precisely request and receive only the data they need, reducing over-fetching and under-fetching issues commonly encountered with traditional RESTful APIs.

In summary: Nest.js, with its GraphQL integration, provides a convenient way to build scalable APIs. TypeScript's static typing enhances code quality and collaboration, while GraphQL's precise data fetching reduces unnecessary requests.
Together, they offer a powerful and efficient approach to developing modern APIs.

## Database
We made the decision to utilize MongoDB as our database of choice, opting for a Non-SQL database solution. Firstly, MongoDB's flexible schema allows for easy and dynamic changes to the configuration settings without requiring predefined table structures. This flexibility is particularly
valuable in situations where the configuration parameters can vary greatly or evolve over time. Additionally, MongoDB's document-oriented model aligns well with the hierarchical nature of configuration data, making it easier to represent and retrieve nested settings. Furthermore, MongoDB's
horizontal scalability and high-performance capabilities make it suitable for handling large-scale configuration data with high read and write demands. Its distributed architecture enables seamless scaling across multiple servers, ensuring robustness and availability. Lastly, MongoDB's
JSON-based query language, coupled with powerful indexing options, provides efficient and flexible ways to retrieve specific configuration settings based on various criteria.

## ODM
Due to our utilization of a Non-SQL database, we opted for an Object Data Manager (ODM) instead of an Object-Relational Mapping (ORM). The distinction lies in the fact that an ORM is employed for relational databases like SQL, while an ODM caters to document databases such as MongoDB.
Initially, we attempted to use Prisma, an ORM for Node.js, but discovered that it didn't integrate smoothly with MongoDB. After conducting a brief search, we came across Mongoose, which is an ODM specifically designed for MongoDB. It proved to be an ideal choice for our needs!

## File structure
```c#
- src
  - DataAccess //The layer that connects to Mongoose ODM
    - Controllers // API endpints controllers 
    - Services // acutal DAL
  - Datamodels //Model/schemas for Mongoose 
  - Modules // Modules for datamodels that have to be resolved  
  - Resolvers // To resolve objects (ex. getting actuall object instead of only ID)
  - seeding // Fuillfill database with fake data
  - app.module.ts // Connects to DB and make use of neccesarry modules
  - main.ts //The main file
- Tests //Tests folder
```
