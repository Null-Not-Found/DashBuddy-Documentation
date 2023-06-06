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
When making this I decided to use a DAL and interfaces but it is overkill. 
Besides, the ORM IS the data access layer so it shouldn't even be here.

