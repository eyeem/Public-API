Sign In
--------

POST http://api.eyeem.com/api/v3/auth/signin HTTP/1.1
email=znarfor@gmail.com&password=XXXXXX

HTTP/1.1 200 OK
{
    "message": "Signed In Successfully",
    "access_token": "eszHxsvh3OuOjpQjGpwkLYFOLnvuXeXx",
    "user": {
        "id": "2ue88m",
        "nickname": "znarf",
        "fullname": "François Hodierne"
    }
}

Authentication Status
---------------------

GET http://api.eyeem.com/api/v3/auth/ok HTTP/1.1
Authorization: Bearer eszHxsvh3OuOjpQjGpwkLYFOLnvuXeXx

If Authenticated:

HTTP/1.1 200 OK
{
    "user": {
        "id": "2ue88m",
        "nickname": "znarf",
        "fullname": "François Hodierne"
    }
}

If Not:

HTTP/1.1 401 Unauthorized
{
    "code": 401,
    "message": "Unauthorized (please authenticate)"
}