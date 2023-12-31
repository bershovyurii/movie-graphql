# movie-graphql
Movie API with GraphQL

Live Server: <https://movie-graphql-server.herokuapp.com/>

Client Code: <https://github.com/bershovyurii/movie-graphql-client>

Client Url: <http://bershovyurii.github.io/movie-graphql-client>

## Schema
```
type Movie {
  id: Int!
  title: String!
  rating: Float
  description_intro: String
  language: String
  medium_cover_image: String
  genres: [String]
}
```

```
type Query {
  movies(limit: Int, rating: Float): [Movie]!
  movie(id: Int!): Movie
  suggestions(id: Int!): [Movie]!
}
```

## Resolvers

1. ```movies: (rating, limit)```
1. ```movie: (id)```
1. ```suggestions: (id)```
