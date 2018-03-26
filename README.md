# EPyTodo - A web ToDo app

- **Repository name:** PSU_minishell1_2017
- **Group size:** 2
- **Repository rigths:** ramassage-tek, lucas.marcel@epitech.eu
- **Language:** Python 3

# Subject

EPyTodo is a project which you could rely on in the future.
Thanks to it, you’ll handle all tasks which you need to do easily!

Into this project, you’ll have to develop:
1. your MySQL database scheme
2. your web server using Flask
3. your HTML pages using Jinja2 (integrated with Flask)

## MySQL Database

Into your database, you’ll need to handle many users with their tasks.

> :exclamation: All instructions have to be **strictly** followed

Create a file named **epytodo.sql**.
You will write into it all your database scheme.
The database name is **epytodo**.
Its tables are named :
1. user
2. task
3. user_has_task

> :bulb: Think about the last one : why do you need this ?
> Maybe it has to do with relationship...

Here are all fields (with types or values) which you must have into your tables:
1. user table
  - _user_id_ (mandatory not null)
  - _username_ (mandatory not null)
  - _password_ (mandatory not null)
  - etc.
2. task table
  - _task_id_ (mandatory not null)
  - _title_ (mandatory not null)
  - _begin_ (optional value when creating a task, actual date by default)
  - _end_ (optional value when creating a task, empty by default)
  - _status_ (**not started** by default / **in progress** / **done**)
  - etc.
3. user_has_task table
  - _fk_user_id_
  - _fk_task_id_

Once your scheme is created, import your file into your MySQL server

```
∼/B-WEB-200> cat epytodo.sql | mysql -u root -p
```

> :exclamation: Your sql file has to be placed at the root folder when turned in.
> Do not insert any records into this file

## Web Server

Files to turn in (refer to the bootstrap to know where placing them into your folders):
- run.py
- __init__.py
- models.py
- views.py
- controller.py

You server will implement a MVC architecture.
There’s not only ONE way to implement it but it’s **mandatory** to do so.
Look closely at schemes you can find. Here’s a [TIP].

More explanations of what is attempted into each file:
- _run.py_ : your entry program
- _&#95;&#95;init&#95;&#95;.py_ : your app package file
- _models.py_ : all objects / functions which will interact with your database
- _views.py_ : all routes which are described into the API file
- _controller.py_ : all interactions between your views and your models

We will add our _config.py_ file.

All settings for your program (debug mode, database configuration, etc.) will be there!
Here are the required ones :
- _DATABASE_NAME_
- _DATABASE_HOST_
- _DATABASE_SOCK_
- _DATABASE_USER_
- _DATABASE_PASS_

Be sure that your _config.py_ is similar and used effectively.

## HTML pages

All data will transit into JSON format (see API file).
You are free to display all information as you want (plain text, lists, accordion, etc.).
This graphical part will be evaluated during your presentation.

# Bonus

> :exclamation: Do not integrate any extra features like allowing PUT or DELETE methods into your main delivery.
> Do this into a bonus directory

Here is a minimal list of what you can do as a bonus:
- add a responsive design
- develop more functionnalities than expected:
  - Ajax requests
  - dynamic components (drag & drop cards, datepickers, etc.)
  - contacts system (adding friends, authorizations handling, etc.)
  - notifications
- implement a real login system (OAuth / SSO / LDAP / etc.)
- develop what’s in your mind

[TIP]: http://lmgtfy.com/?q=MVC