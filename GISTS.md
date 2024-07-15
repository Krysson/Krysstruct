GraphQL Queries & Mutations
These are the GraphQL queries and mutations for the YouTube course.

## Get names of all clients

```
{
  clients {
    name
  }
}
```

## Get a single client name and email

```
{
  client(id: 1) {
    name
    email
  }
}
```

Explain

## Get name and status of all projects

```
{
  projects {
    name
    status
  }
}
```

Explain

## Get a single project name, description along with the client name and email

```
{
  project(id: 1) {
    name
    description,
    client {
      name
      email
    }
  }
}
```

Explain

## Create a new client and return all data

```
mutation {
  addClient(name: "Tony Stark", email: "ironman@gmail.com", phone: "955-365-3376") {
    id
    name
    email
    phone
  }
}
```

Explain

## Delete a client and return id

```
mutation {
  deleteClient(id: 1) {
    id
  }
}
```

Explain

## Create a new project and return name and description

```
mutation {
  addProject(name: "Mobile App", description: "This is the project description", status: "new", clientId: "1") {
   name
   description
  }
}
```

Explain

## Update a project status and return name and status

```
mutation {
  updateProject(status: "completed") {
   name
   status
  }
}
```
