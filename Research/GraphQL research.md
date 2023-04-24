# GraphQL

## Summaries
### Schema Definition: 
A GraphQL API is defined by a schema that describes the types of data available and the relationships between them. The schema is written in the GraphQL Schema Definition Language (SDL). The schema serves as the contract between the client and server, defining what data can be queried and what data can be modified.

### Querying: 
Clients can query the GraphQL API by sending a request to the API endpoint with a GraphQL query string. The query string specifies the data that the client wants to receive and how that data should be structured.

### Execution: 
When the server receives a GraphQL query, it parses the query and maps it to the corresponding parts of the schema. Then, it executes the query and resolves the requested data, returning a response that matches the structure of the query.

### Types and Fields: 
GraphQL has a rich type system that allows developers to define complex types and relationships between them. Types are defined with fields, which represent the data that can be queried for that type.

### Resolver Functions: 
Resolver functions are responsible for fetching the data that corresponds to a particular field in the schema. Resolver functions can be asynchronous and can fetch data from a variety of sources, such as databases or other APIs.

### Mutations: 
In addition to querying data, clients can also modify data through GraphQL using mutations. Mutations are defined in the schema just like queries and can be used to create, update, or delete data.

## Examples
### Schema with Types and Fields Example:
```
type User {
  id: ID!
  name: String!
  email: String!
  posts: [Post!]!
}

type Post {
  id: ID!
  title: String!
  body: String!
  author: User!
}

type Query {
  users: [User!]!
  user(id: ID!): User!
  posts: [Post!]!
  post(id: ID!): Post!
}

type Mutation {
  createUser(name: String!, email: String!): User!
  createPost(title: String!, body: String!, authorId: ID!): Post!
  updatePost(id: ID!, title: String!, body: String!): Post!
  deletePost(id: ID!): Boolean!
}
```
### Querry example:
```
query {
  users {
    id
    name
    posts {
      title
    }
  }
}
```
### Resolver example:
```
const resolvers = {
  User: {
    posts: async (parent, args, context) => {
      const { id } = parent;
      const posts = await context.db.Post.find({ author: id });
      return posts;
    },
  },
};
```
### Mutation example:
```
mutation {
  createUser(name: "Alice", email: "alice@example.com") {
    id
    name
    email
  }
}
```
