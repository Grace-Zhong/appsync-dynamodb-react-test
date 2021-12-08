```
type Post @model {
	id: ID!
	postOwnerId: String!
	postOwnerUsername: String!
	postTitle: String!
	postBody: String!
	createdAt: String
	comments: [Comment] @connection(name: "PostComments") #relationship
	likes: [Like] @connection(name: "PostLikes")
}
 
type Comment @model {
	id: ID!
	commentOwnerId: String!
	commentOwnerUsername: String!
	post: Post @connection(name: "PostComments")
	content: String!
	createdAt: String!
}
 
type Like @model {
	id: ID!
	numberLikes: Int!
	likeOwnerId: String!
	likeOwnerUsername: String!
	post: Post @connection(name: "PostLikes")
}
```
```
GraphQL endpoint: https://xcxw4l5ozja67kprhenncqcb3y.appsync-api.ap-southeast-2.amazonaws.com/graphql
GraphQL API KEY: da2-x7ilhskwbzcpxmlzihghsanf7e
```