# Simple Blog System

The Simple Blog System is a basic web application that allows users to view, create, edit, and delete blog posts. It is built using PHP for the backend and a basic HTML interface for the frontend.

## Table of Contents
1. [Database Setup](#database-setup)
2. [Backend Development](#backend-development)
   - [CRUD for Posts](#crud-for-posts)
3. [Frontend Interface](#frontend-interface)
   - [List of Blog Posts](#list-of-blog-posts)
   - [Add New Post](#add-new-post)
   - [Edit and Delete Posts](#edit-and-delete-posts)
4. [Installation and Setup](#installation-and-setup)
5. [Usage](#usage)

## Database Setup

The database used for this project is MySQL. To set up the database, follow these steps:

1. Create a new database named `BlogDB`:
```sql
CREATE DATABASE BlogDB;
```

2. Create the `posts` table with the following structure:
```sql
USE BlogDB;

CREATE TABLE posts (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  content TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

The SQL setup script for the database is as follows:

```sql
CREATE DATABASE BlogDB;

USE BlogDB;

CREATE TABLE posts (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  content TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Backend Development

The backend of the Simple Blog System is developed using PHP. It handles the server-side logic for the CRUD (Create, Read, Update, Delete) operations on the blog posts.

### CRUD for Posts

1. **Displaying All Posts**:
   - The backend will fetch all the blog posts from the `posts` table in the database and return them in a format that can be displayed on the frontend.

2. **Displaying a Single Post**:
   - The backend will accept a post ID as a parameter and fetch the corresponding blog post from the database. It will then return the post data for display on the frontend.

3. **Creating a New Post**:
   - The backend will accept the title and content of a new blog post from the frontend, and then insert the new post into the `posts` table in the database.

4. **Editing an Existing Post**:
   - The backend will accept the updated title and content of a blog post, along with the post ID, and then update the corresponding record in the `posts` table in the database.

5. **Deleting a Post**:
   - The backend will accept the ID of a blog post and then delete the corresponding record from the `posts` table in the database.

## Frontend Interface

The frontend of the Simple Blog System provides a basic HTML interface for interacting with the backend.

### List of Blog Posts

The frontend will display a list of all the blog posts fetched from the backend. Each post will be displayed with its title, creation date, and a link to view the full post.

### Add New Post

The frontend will provide a form for users to enter a new blog post title and content. When the form is submitted, the backend will be called to create a new post.

### Edit and Delete Posts

The frontend will include options to edit and delete existing blog posts. These options will only be visible to users with admin privileges. When the edit or delete action is triggered, the backend will be called to perform the respective operation.

## Installation and Setup

1. Clone the repository to your local machine:
```
git clone https://github.com/your-username/simple-blog-system.git
```

2. Set up the database:
   - Create the `BlogDB` database and the `posts` table using the SQL script provided in the [Database Setup](#database-setup) section.

3. Configure the database connection in the backend PHP files:
   - Update the database connection details (host, username, password, database name) in the appropriate PHP files.

4. Deploy the project files to your web server or local development environment.

## Usage

1. Open the frontend interface in your web browser. You should see the list of blog posts.

2. To create a new post, click the "Add New Post" link and fill out the form.

3. To view a single post, click on the post title in the list.

4. To edit or delete a post, click the respective buttons next to the post in the list (these options are only visible to admin users).

5. Enjoy your Simple Blog System!
