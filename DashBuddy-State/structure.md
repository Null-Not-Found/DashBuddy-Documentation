# State microservice structure

## contents
- [File structure](#file-structure)

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
