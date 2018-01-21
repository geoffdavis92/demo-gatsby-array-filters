# Demo for Gatsby Array Filters Issue

It would be nice to have the ability to assign arguments onto dynamically-created schemas' node fields that return arrays.

Arguments could be near-identicle to `*Connection` types:

- `skip`
- `limit`
- `sort`
- `filter`

Those existing arguments could be modified to support array-specific needs, like exposure of an `__index`-type field and array index wrapping:

`characters(sort: { fields: [__index], order: ASC }, limit: 2)`

New arguments could also be created to simplify filtering arrays and/or return specific indices:

- `in`: identicle to how this is used in the `*Connection` argument `filter`, except it is applied directly onto the array-returning field (e.g. `characters(in: {name: {eq: "Frodo Baggins"}})`)
- `index`: allow retrieval of specific indices by passing them to `index` in an array (e.g. `characters(index: [0, 1])`, `characters(index: [2])`, `characters(index: [-1])`)

## Getting Started

Install dependencies with `$ yarn`.

Run development server with `$ gatsby develop`.

Access the GraphQL debuggin GUI here: [GUI Link](http://localhost:8000/___graphql).

You can copy/paste queries (linked below) to see this project's data (JSON also linked below).

### Useful links

Data: 

- [JSON files](/src/data/)

Queries: 

- [Experimental GraphQL queries](/src/demoArrayArguments.graphql)
- [Working GraphQL queries](/src/demoQueries.graphql)

