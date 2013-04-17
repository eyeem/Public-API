User
----

GET http://api.eyeem.com/api/v3/users/2ue88m HTTP/1.1

If Existing:

HTTP/1.1 200 OK
{
    "user": {
        "id": "2ue88m",
        "nickname": "znarf",
        "fullname": "François Hodierne"
    }
}

If Not:

HTTP/1.1 404 Not Found
{
    "code": 404,
    "message": "User Not Found"
}

User Photos
-----------

GET http://api.eyeem.com/api/v3/users/2ue88m/photos?limit=2 HTTP/1.1

Supported parameters: offset, limit

HTTP/1.1 200 OK
{
    "photos": {
        "jtt7qz": {
            "user_id": "2ue88m",
            "title": "", << either title or caption. also @mentions.
            "caption": "",
            "filename": "59c5d970bc182306edb57e6a84b98efb4346bf02-1365243713",
            "width": 1296,
            "height": 972,
            "albums": {
                "total": 5,
                "ids": [
                    "9ybug2",
                    "72t7b8",
                    "1ewz4k",
                    "ecco7z",
                    "ts7jzj"
                ]
            },
            "likers": {
                "total": 8,
                "ids": [
                    "loz92",
                    "wjtuxu",
                    "wdjn4q",
                    "nj5lhk",
                    "l9606r",
                    "bjd1p4",
                    "psuiko",
                    "jg8t"
                ]
            },
            "comments": {
                "total": 0,
                "ids": [ ]
            },
            "created": 1365243764
        },
        "ed33je": {
            "user_id": "2ue88m",
            "title": "New Toy",
            "caption": "",
            "filename": "0fb5ebc6fb3a288c193c50943bf44bcae85e55cb-1365089523",
            "width": 1224,
            "height": 1225,
            "albums": {
                "total": 4,
                "ids": [
                    "9ybug2",
                    "72t7b8",
                    "68i7c3",
                    "ecco7z"
                ]
            },
            "likers": {
                "total": 14,
                "ids": [
                    "nj5lhk",
                    "7k6dn0",
                    "zf49pl",
                    "nhrjkj",
                    "rmhpy8",
                    "v5j3s4",
                    "hhf3fw",
                    "2nw3eq",
                    "1m08jn",
                    "wdjn4q",
                    "bjd1p4",
                    "wjtuxu",
                    "xjbk6",
                    "jg8t"
                ]
            },
            "comments": {
                "total": 0,
                "ids": [ ]
            },
            "created": 1365089542
        }
    },
    "users": {
        "2ue88m": { << why are we now using json objects instead of arrays?
            "nickname": "znarf",
            "fullname": "François Hodierne"
        },
        "loz92": {
            "nickname": "Frasier",
            "fullname": "Frasier"
        },
        "wjtuxu": {
            "nickname": "baststock",
            "fullname": "Basti"
        },
        "wdjn4q": {
            "nickname": "boardwaxed",
            "fullname": "Mark Bordeaux"
        },
        "nj5lhk": {
            "nickname": "GiovanniBarbisan",
            "fullname": "Giovanni"
        },
        "l9606r": {
            "nickname": "mixher",
            "fullname": "Marine "
        },
        "bjd1p4": {
            "nickname": "cobras_frogs_bears",
            "fullname": "cobras_frogs_bears"
        },
        "psuiko": {
            "nickname": "inutri",
            "fullname": "inu tri"
        },
        "jg8t": {
            "nickname": "imatias",
            "fullname": "matias"
        },
        "7k6dn0": {
            "nickname": "SiXunderground",
            "fullname": "SixAxiS"
        },
        "zf49pl": {
            "nickname": "Miluna",
            "fullname": "Miluna"
        },
        "nhrjkj": {
            "nickname": "nasser6333",
            "fullname": "alain00009"
        },
        "rmhpy8": {
            "nickname": "gluff",
            "fullname": "G Luff"
        },
        "v5j3s4": {
            "nickname": "julie",
            "fullname": "Julie Landry"
        },
        "hhf3fw": {
            "nickname": "LarsFronius",
            "fullname": "Lars "
        },
        "2nw3eq": {
            "nickname": "Gen",
            "fullname": "Gen Sadakane"
        },
        "1m08jn": {
            "nickname": "spiegeleule",
            "fullname": "Spiegel Eule"
        },
        "xjbk6": {
            "nickname": "tobitos",
            "fullname": "Tobi Poel"
        }
    },
    "comments": [ ],
    "albums": {
        "9ybug2": {
            "type": "country",
            "name": "Germany"
        },
        "72t7b8": {
            "type": "city",
            "name": "Berlin"
        },
        "1ewz4k": {
            "type": "event",
            "name": "Being a hacker at Hasenheide"
        },
        "ecco7z": {
            "type": "venue",
            "name": "Hasenheide"
        },
        "ts7jzj": {
            "type": "tag",
            "name": "Being a hacker"
        },
        "68i7c3": {
            "type": "event",
            "name": "at Hasenheide"
        }
    }
}

User Friends Photos
-------------------

GET http://api.eyeem.com/api/v3/users/2ue88m/friendsPhotos?limit=2 HTTP/1.1

Supported parameters: offset, limit, after, before

HTTP/1.1 200 OK
{
    "photos": {
        "mrnyx9": {
            "user_id": "loz92",
            "title": "",
            "caption": "",
            "filename": "07de562ed56d4f0d1d802b480ba61a7fb92eb911-1365605183",
            "width": 1117,
            "height": 1296,
            "albums": {
                "total": 5,
                "ids": [
                    "9ybug2",
                    "72t7b8",
                    "u1xho",
                    "nabqno",
                    "t6o219"
                ]
            },
            "likers": {
                "total": 0,
                "ids": [ ]
            },
            "comments": {
                "total": 0,
                "ids": [ ]
            },
            "created": 1365605184
        },
        "lm27pf": {
            "user_id": "wxghzy",
            "title": "",
            "caption": "",
            "filename": "ce00e7f81858a9e7eb6837a9c42ded65a926cb3f-1365604012",
            "width": 1152,
            "height": 1152,
            "albums": {
                "total": 3,
                "ids": [
                    "9ybug2",
                    "72t7b8",
                    "i2l0um"
                ]
            },
            "likers": {
                "total": 2,
                "ids": [
                    "k23yah",
                    "ql1ycd"
                ]
            },
            "comments": {
                "total": 0,
                "ids": [ ]
            },
            "created": 1365604027
        }
    },
    "users": {
        "loz92": {
            "nickname": "Frasier",
            "fullname": "Frasier"
        },
        "wxghzy": {
            "nickname": "abelle",
            "fullname": "A-belle"
        },
        "k23yah": {
            "nickname": "iamluys",
            "fullname": "Luys Miguel"
        },
        "ql1ycd": {
            "nickname": "Flo",
            "fullname": "Flo Meissner"
        }
    },
    "comments": [ ],
    "albums": {
        "9ybug2": {
            "type": "country",
            "name": "Germany"
        },
        "72t7b8": {
            "type": "city",
            "name": "Berlin"
        },
        "u1xho": {
            "type": "event",
            "name": "Taking Photos at Berlin"
        },
        "nabqno": {
            "type": "venue",
            "name": "Berlin"
        },
        "t6o219": {
            "type": "tag",
            "name": "Taking Photos"
        },
        "i2l0um": {
            "type": "tag",
            "name": "Shopping"
        }
    }
}