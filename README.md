# Superheroes API – Phase 4 Week 1 Code Challenge

#### Date: 5/1/2026

#### By *Judy Ogachi*

## Project Overview

This project is a Flask REST API that manages Heroes, Powers, and their many-to-many relationship through HeroPowers.
It is built using Flask, SQLAlchemy, Flask-Migrate, and SQLite.

The API fully satisfies the requirements of the Phase 4 Week 1 Superheroes Code Challenge and can be tested using the included Postman collection.

## Features

RESTful API endpoints for Heroes, Powers, and HeroPowers

Many-to-many relationship between Heroes and Powers

Model validations and error handling

Database migrations with Flask-Migrate

Database seeding

Postman collection for endpoint testing

## Postman Collection

This repository includes a Postman collection for testing all required endpoints.

1. Importing the Collection

2. Open Postman

3. lick Import

4. Select Upload Files

5. Choose Code_Challenge_Superheroes

6. Click Import

Use the collection to test all routes once the server is running.

## Database Models
Hero
* id
* name
* super_name

has many Powers through HeroPower

Power
* id
* name
* description

has many Heros through HeroPower

HeroPower

* id
* strength (Strong, Weak, or Average)
* hero_id
* power_id

belongs to a Hero

belongs to a Power

Cascade deletes are configured so that dependent records are removed automatically.

## Database Setup
Install dependencies
```
pipenv install
pipenv shell
```
Run migrations
```
flask db init
flask db migrate
flask db upgrade
```

Seed the database
```
python server/seed.py
```

## Running the Server
```
cd server
flask run
```

The server runs on:

http://localhost:5555

## Support and contact details
github.com/Bonarerijt

### License
MIT License

Copyright (c) 2026 Bonarerijt

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
