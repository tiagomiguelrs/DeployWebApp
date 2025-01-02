# Flask Blog Application with User Authentication

## Description
This project is a blog application built using the Flask framework. It allows users to register, log in, create, edit, and delete blog posts. The application also supports commenting on posts and includes user authentication and authorization features. It uses SQLAlchemy for database management, Flask-Login for user session management, and Flask-WTF for form handling and validation.

## Features

User Registration and Login: Allows users to register and log in to the application.

Create, Edit, and Delete Posts: Authenticated users can create, edit, and delete blog posts. Only admin users can perform these actions.

Commenting: Authenticated users can comment on blog posts.

User Authentication: Uses Flask-Login to manage user sessions and ensure only authenticated users can access certain features.

Admin Authorization: Uses a custom decorator to restrict certain actions (like creating, editing, and deleting posts) to admin users only.

Email Notifications: Sends email notifications when a user submits a contact form.

Profile Images: Uses Gravatar to add profile images to the comment section.

Rich Text Editing: Integrates CKEditor for rich text editing in blog posts.

## How It Works
Home Page: The home page displays a list of all blog posts.

User Registration: The `/register` route allows new users to register by providing their email, name, and password.

User Login: The `/login` route allows existing users to log in by providing their email and password.

User Logout: The `/logout` route logs out the current user.

Create Post: The `/new-post` route allows admin users to create new blog posts.

Edit Post: The `/edit-post/<int:post_id>` route allows admin users to edit existing blog posts.

Delete Post: The `/delete/<int:post_id>` route allows admin users to delete blog posts.

View Post: The `/post/<int:post_id>` route displays a single blog post and its comments. Authenticated users can add comments.

About Page: The `/about` route displays an about page.

Contact Page: The `/contact` route displays a contact form. When the form is submitted, an email is sent to the blog owner.
