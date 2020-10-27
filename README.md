# NickFlix

## Overview

This project pretends to be an replica of Netflix, but instead of streaming videos, movies, it will stream musics clips, discographies. Filtered by genre, artist, and some other things..

The repository contains the API Rest that are NickFlix Back-End, developed in PHP with Laravel.

##### Current project status

Because of time, the project its unfinished yet, theres some of these follow things left that i'm still working on.

- JWT authentication
- Improve middlewares
- Create Routes and implementation to account and content management

---

## Setup

To install the project, after clone the repo, you must run 

```
composer install
```

After install the project, you must create an **.env** file in the root folder, it can be quickly done with `cat > .env.example > .env` in your UNIX terminal, otherwise, you can mannually copy and paste **.env.example** as **.env**

The **env** file contains environment variables that are used by PHP and Laravel, pay attention to **DATABASE** keys, fill then with the username and password of your MySQL DB local server. 

Now, with your MySQL database local server running, you must run

```
php artisan key:generate

php artisan migrate
```

It will create the tables to your database.

### Running

To run the project, first we must addopting the project url as **api.nickflix:8001**, but to reach that URL to our local machine and it be recognized through our serve application, it must be added as Super User/ADM to `/etc/hosts` of your **S.O** (In Windows it must be at `C:\Windows\System32\drivers\etc`) the follow line (It can be added to a new last line) `127.0.0.2   api.nickflix`

Now with the url visible, you must run

```
php artisan --host=api.nickflix --port=8001
```

If everything goes right, try to access (GET Request through Postman) [api.nickflix:8001](api.nickflix:8001), it must returning the follow JSON:

```
{
    "message" : "Hello Worldson =]"
}
```