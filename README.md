# **API for YaTube**
## **Description**
API for interacting with **YaTube**(https://github.com/hilaaba/api_final_yatube.git) project.
### Authors
Ivanov Vyacheslav
## **How to start the project**
Clone the repository and go to it on the command line:
```
git clone https://github.com/hilaaba/api_final_yatube.git
```
```
cd api_yatube
```
Create and activate a venv:
```
python3 -m venv venv
```
```
source venv/bin/activate or source venv/Scripts/activate
```
Install dependencies from a file requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
python3 -m pip install -r requirements.txt
```
Perform migrations:
```
python3 manage.py migrate
```
Launch a project:
```
python3 manage.py runserver
```
## **Requirements**
```
Django==2.2.16
django-filter==21.1
djangorestframework==3.12.4
djangorestframework-simplejwt==4.7.2
djoser
Pillow==8.3.1
PyJWT==2.1.0
requests==2.26.0
```

### Technologies
- Python 3.9
- Django 2.2.16
- Djangorestframework 3.12.4

## **Examples of API requests**
```
GET /api/v1/posts/
```
**Response sample**
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
---
```
POST /api/v1/posts/
```
**Request sample**
```
}
    "text": "string",
    "image": "string",
    "group": 0
}
```
**Response sample**
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
---
```
PUT /api/v1/posts/{id}/
```
**Request sample**
```
{
    "text": "stringstring",
    "image": "string",
    "group": 0
}
```
**Response sample**
```
{
    "id": 0,
    "author": "stringstring",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
---
```
PATCH /api/v1/posts/{id}/
```
**Request sample**
```
{
    "text": "anotherstring"
}
```
**Response sample**
```
{
    "id": 0,
    "author": "stringstring",
    "text": "anotherstring",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
---
```
DELETE /api/v1/posts/{id}/
```
---
```
GET /api/v1/posts/{post_id}/comments/
```
**Response sample**
```
[
    {
        "id": 0,
        "author": "string",
        "text": "string",
        "created": "2019-08-24T14:15:22Z",
        "post": 0
    }
]
```
---
```
POST /api/v1/posts/{post_id}/comments/
```
**Request sample**
```
{
    "text": "string"
}
```
**Response sample**
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
}
```
---
```
POST /api/v1/jwt/create/
```
**Request sample**
```
{
    "username": "string",
    "password": "string"
}
```
**Response sample**
```
{
    "refresh": "string",
    "access": "string"
}
```

### License
MIT License

Copyright (c) 2022 Ivanov Vyacheslav

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