# Spring Boot, MySQL, Spring Security, JWT, JPA, Rest API

Restful CRUD API for a blog using Spring Boot, Mysql, JPA and Hibernate.


## Explore Rest APIs

The app defines following CRUD APIs.

### Auth

| Method | Url | Decription | 
| ------ | --- | ---------- |
| POST   | /api/auth/signup | Sign up |
| POST   | /api/auth/signin | Log in |

### Users

| Method | Url | Description |
| ------ | --- | ----------- |
| GET    | /api/users/me | Get logged in user profile |
| GET    | /api/users/{username}/profile | Get user profile by username |
| GET    | /api/users/{username}/posts | Get posts created by user |
| GET    | /api/users/{username}/albums | Get albums created by user |
| GET    | /api/users/checkUsernameAvailability | Check if username is available to register |
| GET    | /api/users/checkEmailAvailability | Check if email is available to register |
| POST   | /api/users | Add user (Only for admins) |
| PUT    | /api/users/{username} | Update user (If profile belongs to logged in user or logged in user is admin) |
| DELETE | /api/users/{username} | Delete user (For logged in user or admin) |
| PUT    | /api/users/{username}/giveAdmin | Give admin role to user (only for admins) |
| PUT    | /api/users/{username}/TakeAdmin | Take admin role from user (only for admins) |
| PUT    | /api/users/setOrUpdateInfo | Update user profile (If profile belongs to logged in user or logged in user is admin) |

### Posts

| Method | Url | Description |
| ------ | --- | ----------- |
| GET    | /api/posts | Get all posts |
| GET    | /api/posts/{id} | Get post by id |
| POST   | /api/posts | Create new post (By logged in user) |
| PUT    | /api/posts/{id} | Update post (If post belongs to logged in user or logged in user is admin) |
| DELETE | /api/posts/{id} | Delete post (If post belongs to logged in user or logged in user is admin) |

### Comments

| Method | Url | Description |
| ------ | --- | ----------- |
| GET    | /api/posts/{postId}/comments | Get all comments which belongs to post with id = postId |
| GET    | /api/posts/{postId}/comments/{id} | Get comment by id if it belongs to post with id = postId |
| POST   | /api/posts/{postId}/comments | Create new comment for post with id = postId (By logged in user) |
| PUT    | /api/posts/{postId}/comments/{id} | Update comment by id if it belongs to post with id = postId (If comment belongs to logged in user or logged in user is admin) |
| DELETE | /api/posts/{postId}/comments/{id} | Delete comment by id if it belongs to post with id = postId (If comment belongs to logged in user or logged in user is admin) |

### Albums

| Method | Url | Description |
| ------ | --- | ----------- |
| GET    | /api/albums | Get all albums |
| GET    | /api/albums/{id} | Get album by id |
| POST   | /api/albums | Create new album (By logged in user) |
| PUT    | /api/albums/{id} | Update album (If album belongs to logged in user or logged in user is admin) |
| DELETE | /api/albums/{id} | Delete album (If album belongs to logged in user or logged in user is admin) |
| GET    | /api/albums/{id}/photos | Get all photos which belongs to album with id = id |

### Photos

| Method | Url | Description |
| ------ | --- | ----------- |
| GET    | /api/photos | Get all photos |
| GET    | /api/photos/{id} | Get photo by id |
| POST   | /api/photos | Create new photo (By logged in user) |
| PUT    | /api/photos/{id} | Update photo (If photo belongs to logged in user or logged in user is admin) |
| DELETE | /api/photos/{id} | Delete photo (If photo belongs to logged in user or logged in user is admin) |

### Todos

| Method | Url | Description |
| ------ | --- | ----------- |
| GET    | /api/todos | Get all todos which belongs to logged in user |
| GET    | /api/todos/{id} | Get todo by id (If todo belongs to logged in user) |
| POST   | /api/todos | Create new todo (By logged in user) |
| PUT    | /api/todos/{id} | Update todo (If todo belongs to logged in user) |
| DELETE | /api/todos/{id} | Delete todo (If todo belongs to logged in user) |
| PUT    | /api/todos/{id}/complete | Mark todo as complete (If todo belongs to logged in user) |
| PUT    | /api/todos/{id}/unComplete | Mark todo as uncomplete (If todo belongs to logged in user) |
