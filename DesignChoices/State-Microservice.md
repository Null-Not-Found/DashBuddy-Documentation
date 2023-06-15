# State-Microservice design choices

## Language
Node.js, TypeScript, and Express form a powerful combination for constructing web applications. Node.js facilitates code reuse and streamlines the development process. TypeScript, with its static typing capabilities, aids in catching errors during development and improves code maintainability. The ability to define types and interfaces enhances code readability and promotes seamless collaboration within teams. Express, a minimalist web application framework for Node.js, simplifies the creation of robust APIs, handling routing and middleware efficiently. It offers a solid foundation for building scalable and modular applications, allowing developers to focus on business logic rather than boilerplate code. Additionally, Express's lightweight nature contributes to fast response times and high performance. 

In summary, the amalgamation of Node.js, TypeScript, and Express creates a productive and scalable environment for developing efficient web applications.

## Database
We made the decision to utilize MongoDB as our database of choice, opting for a Non-SQL database solution. Firstly, MongoDB's flexible schema allows for easy and dynamic changes to the configuration settings without requiring predefined table structures. This flexibility is particularly valuable in situations where the configuration parameters can vary greatly or evolve over time. Additionally, MongoDB's document-oriented model aligns well with the hierarchical nature of configuration data, making it easier to represent and retrieve nested settings. Furthermore, MongoDB's horizontal scalability and high-performance capabilities make it suitable for handling large-scale configuration data with high read and write demands. Its distributed architecture enables seamless scaling across multiple servers, ensuring robustness and availability. Lastly, MongoDB's JSON-based query language, coupled with powerful indexing options, provides efficient and flexible ways to retrieve specific configuration settings based on various criteria.

## ODM
Due to our utilization of a Non-SQL database, we opted for an Object Data Manager (ODM) instead of an Object-Relational Mapping (ORM). The distinction lies in the fact that an ORM is employed for relational databases like SQL, while an ODM caters to document databases such as MongoDB. Initially, we attempted to use Prisma, an ORM for Node.js, but discovered that it didn't integrate smoothly with MongoDB. After conducting a brief search, we came across Mongoose, which is an ODM specifically designed for MongoDB. It proved to be an ideal choice for our needs!

### File structure
```c#
- src
  - DAl //The layer that connects to Mongoose ODM
  - DAl Interfaces //interface layer for the DAl
  - Models //Model/schemas for Mongoose 
  - server.ts //The main file
- Tests //Tests folder
```
During the development process, I initially opted to incorporate a Data Access Layer (DAL) and interfaces. However, upon further consideration, I realized that it was unnecessary and excessive for our requirements. Additionally, the ODM itself functions as the data access layer, rendering the inclusion of a separate DAL redundant.
