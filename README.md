Flask Blog

A full-stack Flask blog with user authentication, posts (CKEditor), comments with Gravatar avatars, and admin-only post management. 
Ships with a simple Bootstrap UI and SQLAlchemy models.

Features
- Register/Login/Logout with hashed passwords (PBKDF2).
- Create, edit, delete posts (CKEditor).
- Logged-in users can comment; use avatars via Gravatar.
- @admin_only routes; user with id == 1 is treated as admin.
- Bootstrap 5 + Flask-Bootstrap integration.
- SQLite (default) or PostgreSQL via env (DB_URI).

Technology
- Flask, Flask-Login, Flask-WTF (forms), Flask-CKEditor, Flask-Bootstrap
- SQLAlchemy, SQLite / PostgreSQL
- PBKDF2 Password Hashing
- Gravatar for user avatars

("/")	GET:	List all posts
("/register")	GET, POST:	Create account
("/login") GET, POST:	Login
("/logout")	GET:	Logout
("/post/<int:post_id>")	GET, POST:	View a post, add comments
("/new-post")	GET, POST:	Create a post. Admin only (id == 1)
("/edit-post/<int:post_id>")	GET, POST:	Edit a post.	Admin only
("/delete/<int:post_id>")	GET:	Delete a post.	Admin only
("/about")	GET:	About page
("/contact")	GET, POST:	Contact form (sends email)
