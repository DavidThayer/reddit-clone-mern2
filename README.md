# Reddit Clone – MERN stack
Building a Reddit clone using MERN stack


## Back-End: Node, Express, and MongoDB (Mongoose)
1. Use Express to set up a basic Node server that fetches data from MongoDB
2. Make sure MongoDB is running (`mongod`), then start your Node server
2. Create `TextPost` resource
  1. Create a `TextPost` model that contains `title`, `content`, `thumbnail_image_url`, `votes`
  2. Add the following API CRUD routes for `Posts`
    - `/api/posts` – GET, POST
    - `api/posts/:post_id` – GET, PUT, DELETE
  3. Fill out the `Posts` controller using Mongoose queries
4. Create `Comment` resource
  1. Create a `Comment` model that contains `content`, `post_id`
  2. Add the following API CRUD routes for `Comments`
    - `/api/posts/:post_id/comments` – GET, POST
    - `api/posts/:post_id/comments/:comment_id` – GET, PUT, DELETE
  3. Fill out the `Comments` controller using Mongoose queries
5. Use POSTMAN to create a `Post` and a `Comment`


## Front-End: React
1. Set up a basic React app
3. Pul in React router to implement the following routes
  - `/` – Should show home dashboard where posts' titles and thumbnail images are displayed
  - `/posts/:post_id` – Clicking on a post should redirect to its show page (all post content, attached comments, and form for adding comments)
4. Implement the following user stories
  - User should see all posts on the home page
  - User should be able to click on a "Create Post" button and see a modal to create a new post
  - User should be able to comment on a post
  - User should be able to comment on a comment (requires adding field to `Comment` model)

## BONUS
1. Create a `LinkPost` resource
2. Create a `User` resource 
  - Should have fields `first_name`, `last_name`, `email`, and `password_hash`
  - Implement authentication
  - Both `Post` and `Comment` should have `author_id` (views should also include author names)
3. Implement a `SubReddit` model
  - Should have `name` and `slug` (e.g. 'Software Engineering', 'software-engineering')
  - `Post` should have a `subreddit_id`
