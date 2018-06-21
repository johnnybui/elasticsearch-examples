# Match all
GET employees/_search
{
  "query": {
    "match_all": {}
  }
}

# Create index
PUT employees

# Delete index
DELETE employees

# Create document
POST employees/doc
{
  "id": "5b2b519d5e43648f09be4a27",
  "index": 0,
  "guid": "144f2f76-3363-4e62-80d5-e847aa8f2856",
  "isActive": false,
  "balance": "$1,436.39",
  "picture": "http://placehold.it/32x32",
  "age": 34,
  "eyeColor": "blue",
  "name": "Webster Koch",
  "gender": "male",
  "company": "GALLAXIA",
  "email": "websterkoch@gallaxia.com",
  "phone": "+1 (938) 580-2652",
  "address": "519 Cooper Street, Eagletown, Puerto Rico, 7728",
  "registered": "2015-07-19T04:16:46 -07:00",
  "latitude": 51.673448,
  "longitude": 49.975534,
  "tags": [
    "minim",
    "non",
    "elit",
    "qui",
    "anim",
    "proident",
    "ex"
  ],
  "friends": [
    {
      "id": 0,
      "name": "Delores Berger"
    },
    {
      "id": 1,
      "name": "Carlson Hernandez"
    },
    {
      "id": 2,
      "name": "Benson Mcpherson"
    }
  ],
  "greeting": "Hello, Webster Koch! You have 9 unread messages.",
  "favoriteFruit": "strawberry"
}

# Set document
PUT employees/doc/1234
{
  "id": "5b2b519d5e43648f09be4a27",
  "index": 0,
  "guid": "144f2f76-3363-4e62-80d5-e847aa8f2856",
  "isActive": false,
  "balance": "$1,436.39",
  "picture": "http://placehold.it/32x32",
  "age": 34,
  "eyeColor": "blue",
  "name": "Webster Koch",
  "gender": "male",
  "company": "GALLAXIA",
  "email": "websterkoch@gallaxia.com",
  "phone": "+1 (938) 580-2652",
  "address": "519 Cooper Street, Eagletown, Puerto Rico, 7728",
  "registered": "2015-07-19T04:16:46 -07:00",
  "latitude": 51.673448,
  "longitude": 49.975534,
  "tags": [
    "minim",
    "non",
    "elit",
    "qui",
    "anim",
    "proident",
    "ex"
  ],
  "friends": [
    {
      "id": 0,
      "name": "Delores Berger"
    },
    {
      "id": 1,
      "name": "Carlson Hernandez"
    },
    {
      "id": 2,
      "name": "Benson Mcpherson"
    }
  ],
  "greeting": "Hello, Webster Koch! You have 9 unread messages.",
  "favoriteFruit": "strawberry"
}

PUT employees/doc/1234
{
  "id": "5b2b519de6c4ad67904e3fec",
  "index": 1,
  "guid": "f1811a91-ea1f-42c9-b6d3-e0837815885c",
  "isActive": false,
  "balance": "$1,848.93",
  "picture": "http://placehold.it/32x32",
  "age": 28,
  "eyeColor": "blue",
  "name": "Selma Vance",
  "gender": "female",
  "company": "EMTRAK",
  "email": "selmavance@emtrak.com",
  "phone": "+1 (973) 529-3097",
  "address": "464 Boerum Place, Bendon, Massachusetts, 1345",
  "registered": "2016-06-26T10:20:01 -07:00",
  "latitude": -42.20503,
  "longitude": 165.945966,
  "tags": [
    "incididunt",
    "laboris",
    "magna",
    "anim",
    "deserunt",
    "dolor",
    "dolore"
  ],
  "friends": [
    {
      "id": 0,
      "name": "Reese Alford"
    },
    {
      "id": 1,
      "name": "Juliana Vargas"
    },
    {
      "id": 2,
      "name": "Elsa Rollins"
    }
  ],
  "greeting": "Hello, Selma Vance! You have 4 unread messages.",
  "favoriteFruit": "banana"
}

# Bulk import
POST _bulk
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b5333305279514dc3e75b","index":0,"guid":"2f2b585b-d726-479d-894d-d1e152a22cd4","isActive":false,"balance":"$3,260.35","picture":"http://placehold.it/32x32","age":29,"eyeColor":"brown","name":"Liza Pitts","gender":"female","company":"PRIMORDIA","email":"lizapitts@primordia.com","phone":"+1 (981) 520-3295","address":"427 Georgia Avenue, Sidman, Maryland, 7858","registered":"2014-05-08T08:09:59 -07:00","latitude":-45.806985,"longitude":126.063409,"tags":["officia","ullamco","aliquip","magna","velit","irure","id"],"friends":[{"id":0,"name":"Harvey Goodwin"},{"id":1,"name":"Duke Carson"},{"id":2,"name":"Celina Fleming"}],"greeting":"Hello, Liza Pitts! You have 1 unread messages.","favoriteFruit":"strawberry"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b5333db00825e527ea227","index":1,"guid":"b12b9190-4b88-4a4c-aa30-954e52b6098b","isActive":false,"balance":"$1,777.25","picture":"http://placehold.it/32x32","age":24,"eyeColor":"blue","name":"Josefina Burton","gender":"female","company":"GRONK","email":"josefinaburton@gronk.com","phone":"+1 (843) 401-2120","address":"277 Elliott Walk, Tooleville, Washington, 8569","registered":"2015-04-23T09:35:57 -07:00","latitude":-4.77879,"longitude":14.415291,"tags":["consectetur","aliqua","tempor","ex","anim","sunt","velit"],"friends":[{"id":0,"name":"Cobb Perkins"},{"id":1,"name":"Sharp Sanchez"},{"id":2,"name":"Garrett Rowe"}],"greeting":"Hello, Josefina Burton! You have 5 unread messages.","favoriteFruit":"apple"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b533372c24c4cd4fc5f59","index":2,"guid":"4abebf9d-3e3a-4af2-858c-f12328effc88","isActive":true,"balance":"$3,458.85","picture":"http://placehold.it/32x32","age":28,"eyeColor":"brown","name":"Callie Munoz","gender":"female","company":"QOT","email":"calliemunoz@qot.com","phone":"+1 (823) 409-2257","address":"228 Broadway , Garberville, Wisconsin, 5470","registered":"2016-04-09T05:55:43 -07:00","latitude":14.980532,"longitude":15.034338,"tags":["culpa","culpa","irure","laboris","quis","laboris","incididunt"],"friends":[{"id":0,"name":"Hodges Garcia"},{"id":1,"name":"Alyson Mclaughlin"},{"id":2,"name":"Laurie Gaines"}],"greeting":"Hello, Callie Munoz! You have 4 unread messages.","favoriteFruit":"strawberry"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b5333b2db9e26d581c2f2","index":3,"guid":"59581e4a-b25a-4a02-9ae6-6ec96badee51","isActive":false,"balance":"$3,698.86","picture":"http://placehold.it/32x32","age":23,"eyeColor":"brown","name":"Jeanette Kaufman","gender":"female","company":"EQUITOX","email":"jeanettekaufman@equitox.com","phone":"+1 (865) 574-2633","address":"264 Hastings Street, Boykin, Indiana, 9162","registered":"2014-07-07T12:42:54 -07:00","latitude":-48.667613,"longitude":18.471818,"tags":["labore","velit","mollit","anim","laborum","elit","quis"],"friends":[{"id":0,"name":"Amber Jefferson"},{"id":1,"name":"Deirdre Lindsay"},{"id":2,"name":"Mills Leonard"}],"greeting":"Hello, Jeanette Kaufman! You have 9 unread messages.","favoriteFruit":"apple"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b53333f9b688dafc53298","index":4,"guid":"dc5f5c9d-b762-463e-8a70-b97e47772ccf","isActive":true,"balance":"$3,988.72","picture":"http://placehold.it/32x32","age":37,"eyeColor":"brown","name":"Lupe Edwards","gender":"female","company":"SOPRANO","email":"lupeedwards@soprano.com","phone":"+1 (804) 529-2867","address":"329 Dekalb Avenue, Lynn, Marshall Islands, 3620","registered":"2015-08-30T10:44:43 -07:00","latitude":-1.8726,"longitude":-58.543918,"tags":["velit","mollit","magna","enim","nostrud","qui","mollit"],"friends":[{"id":0,"name":"Patsy Cohen"},{"id":1,"name":"Buckner Nicholson"},{"id":2,"name":"Puckett Raymond"}],"greeting":"Hello, Lupe Edwards! You have 4 unread messages.","favoriteFruit":"banana"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c4d8f1e6acd776fa84","index":0,"guid":"a4fd0c26-5272-425a-9b44-ab93b7121e74","isActive":false,"balance":"$3,456.86","picture":"http://placehold.it/32x32","age":40,"eyeColor":"green","name":"Deleon Joyner","gender":"male","company":"ZBOO","email":"deleonjoyner@zboo.com","phone":"+1 (931) 511-3005","address":"589 Neptune Court, Ruffin, Ohio, 2781","registered":"2017-01-08T09:49:32 -07:00","latitude":-80.762158,"longitude":146.353666,"tags":["commodo","consequat","culpa","voluptate","tempor","nisi","ad"],"friends":[{"id":0,"name":"Sophia Larsen"},{"id":1,"name":"Fanny Dyer"},{"id":2,"name":"Washington Walter"}],"greeting":"Hello, Deleon Joyner! You have 2 unread messages.","favoriteFruit":"strawberry"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c45f69d030c3d924e8","index":1,"guid":"86c49c79-b663-493d-ad19-26dcc795dc49","isActive":false,"balance":"$3,287.17","picture":"http://placehold.it/32x32","age":28,"eyeColor":"blue","name":"Winifred Orr","gender":"female","company":"NIKUDA","email":"winifredorr@nikuda.com","phone":"+1 (829) 488-2918","address":"950 Portal Street, Topanga, Mississippi, 3531","registered":"2016-11-23T05:00:48 -07:00","latitude":-53.122924,"longitude":-82.108118,"tags":["cupidatat","voluptate","ut","elit","aute","est","minim"],"friends":[{"id":0,"name":"Briana Mosley"},{"id":1,"name":"Larsen Hess"},{"id":2,"name":"Nanette Mercado"}],"greeting":"Hello, Winifred Orr! You have 6 unread messages.","favoriteFruit":"apple"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c4474bad20136f2fbd","index":2,"guid":"853f2343-de3a-4cf9-aea6-f4f780092d87","isActive":true,"balance":"$2,333.28","picture":"http://placehold.it/32x32","age":26,"eyeColor":"green","name":"Luella Curry","gender":"female","company":"UNCORP","email":"luellacurry@uncorp.com","phone":"+1 (845) 566-3372","address":"736 Victor Road, Osage, Massachusetts, 9523","registered":"2014-04-11T11:34:13 -07:00","latitude":-27.665126,"longitude":-54.639342,"tags":["deserunt","aliqua","eiusmod","voluptate","velit","enim","esse"],"friends":[{"id":0,"name":"Bryant Cannon"},{"id":1,"name":"Stone Holcomb"},{"id":2,"name":"Vega Daniels"}],"greeting":"Hello, Luella Curry! You have 10 unread messages.","favoriteFruit":"apple"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c44006dd188757d958","index":3,"guid":"88cdeddc-bdd9-4fdb-87f1-cb3624a8e6b7","isActive":false,"balance":"$3,675.94","picture":"http://placehold.it/32x32","age":36,"eyeColor":"blue","name":"Humphrey Solis","gender":"male","company":"CHORIZON","email":"humphreysolis@chorizon.com","phone":"+1 (809) 541-3917","address":"484 Perry Terrace, Corinne, Louisiana, 8172","registered":"2016-11-21T01:30:41 -07:00","latitude":-27.513189,"longitude":130.830241,"tags":["dolor","dolor","ipsum","dolor","voluptate","est","eu"],"friends":[{"id":0,"name":"Ines Mccarty"},{"id":1,"name":"Anthony Sparks"},{"id":2,"name":"Perez Becker"}],"greeting":"Hello, Humphrey Solis! You have 6 unread messages.","favoriteFruit":"apple"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c4a9503a5f77c10ce8","index":4,"guid":"878e52d1-b436-457b-b335-36fb97185d16","isActive":true,"balance":"$1,931.39","picture":"http://placehold.it/32x32","age":29,"eyeColor":"green","name":"Odom Newman","gender":"male","company":"COMTRAK","email":"odomnewman@comtrak.com","phone":"+1 (894) 492-3118","address":"682 Dupont Street, Biehle, Virgin Islands, 4252","registered":"2017-08-24T02:45:29 -07:00","latitude":61.660666,"longitude":26.389093,"tags":["id","quis","consectetur","duis","eiusmod","ad","cupidatat"],"friends":[{"id":0,"name":"Alejandra Page"},{"id":1,"name":"Karin Freeman"},{"id":2,"name":"Christina Harmon"}],"greeting":"Hello, Odom Newman! You have 4 unread messages.","favoriteFruit":"banana"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c40750429f544d9663","index":5,"guid":"9c51d5ff-ada4-42dc-98c9-9b3bde14f484","isActive":true,"balance":"$2,461.85","picture":"http://placehold.it/32x32","age":40,"eyeColor":"brown","name":"Sonia Alford","gender":"female","company":"CANDECOR","email":"soniaalford@candecor.com","phone":"+1 (820) 584-2310","address":"101 Delevan Street, Sylvanite, Palau, 6556","registered":"2018-05-03T11:23:04 -07:00","latitude":-84.141065,"longitude":176.89636,"tags":["id","ex","ullamco","Lorem","ipsum","incididunt","mollit"],"friends":[{"id":0,"name":"Gentry Hendricks"},{"id":1,"name":"Earlene Harper"},{"id":2,"name":"Carrie Allison"}],"greeting":"Hello, Sonia Alford! You have 6 unread messages.","favoriteFruit":"banana"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c44973876fae03de2b","index":6,"guid":"6e72633b-1c61-43f6-ad80-dc1ac7dc7e44","isActive":true,"balance":"$2,420.99","picture":"http://placehold.it/32x32","age":26,"eyeColor":"blue","name":"Freda Thomas","gender":"female","company":"SYNTAC","email":"fredathomas@syntac.com","phone":"+1 (922) 579-2356","address":"503 Sheffield Avenue, Canterwood, Illinois, 8962","registered":"2017-11-21T07:02:28 -07:00","latitude":-24.28437,"longitude":127.655904,"tags":["aliquip","ea","eiusmod","elit","non","excepteur","cillum"],"friends":[{"id":0,"name":"Bowers Porter"},{"id":1,"name":"Celeste Stark"},{"id":2,"name":"Rodriguez Hahn"}],"greeting":"Hello, Freda Thomas! You have 1 unread messages.","favoriteFruit":"strawberry"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c4494170552c18affa","index":7,"guid":"7f12c7bc-3b67-46a8-b733-b370b42eec3f","isActive":true,"balance":"$3,426.50","picture":"http://placehold.it/32x32","age":23,"eyeColor":"green","name":"Aurora Gentry","gender":"female","company":"COMTREK","email":"auroragentry@comtrek.com","phone":"+1 (873) 407-3292","address":"969 Imlay Street, Grahamtown, New Hampshire, 6205","registered":"2017-05-20T05:11:25 -07:00","latitude":40.391727,"longitude":-55.82318,"tags":["tempor","fugiat","ipsum","consequat","et","deserunt","ut"],"friends":[{"id":0,"name":"Rosario Gonzales"},{"id":1,"name":"Letitia Garza"},{"id":2,"name":"Blevins Taylor"}],"greeting":"Hello, Aurora Gentry! You have 8 unread messages.","favoriteFruit":"strawberry"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c447b10fc990778a64","index":8,"guid":"c22b4be1-8612-454c-b4c7-2e219ca725bb","isActive":false,"balance":"$2,115.59","picture":"http://placehold.it/32x32","age":37,"eyeColor":"brown","name":"Kinney Giles","gender":"male","company":"ZENTIME","email":"kinneygiles@zentime.com","phone":"+1 (880) 446-3001","address":"577 Nassau Street, Forestburg, Montana, 3954","registered":"2015-04-22T10:26:31 -07:00","latitude":-83.132626,"longitude":-129.523977,"tags":["mollit","eiusmod","elit","velit","qui","reprehenderit","officia"],"friends":[{"id":0,"name":"Willie Wagner"},{"id":1,"name":"Marilyn Duffy"},{"id":2,"name":"Frieda Harrison"}],"greeting":"Hello, Kinney Giles! You have 3 unread messages.","favoriteFruit":"banana"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c417013d77722392b7","index":9,"guid":"8238f100-c9ab-4cd3-8e69-138a9c999dcb","isActive":true,"balance":"$2,674.81","picture":"http://placehold.it/32x32","age":28,"eyeColor":"green","name":"Milagros Camacho","gender":"female","company":"VORATAK","email":"milagroscamacho@voratak.com","phone":"+1 (832) 486-2468","address":"215 Gardner Avenue, Steinhatchee, Kentucky, 2395","registered":"2014-12-07T05:28:27 -07:00","latitude":-55.783214,"longitude":-50.23055,"tags":["consectetur","nisi","reprehenderit","ea","laboris","dolor","non"],"friends":[{"id":0,"name":"Daisy Saunders"},{"id":1,"name":"Lang Hale"},{"id":2,"name":"Berg Moran"}],"greeting":"Hello, Milagros Camacho! You have 2 unread messages.","favoriteFruit":"strawberry"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c47d427955b4e350d8","index":10,"guid":"f8d7d478-b484-4cbd-8099-a5c2c4acb513","isActive":true,"balance":"$3,580.58","picture":"http://placehold.it/32x32","age":20,"eyeColor":"blue","name":"Bernadette Mann","gender":"female","company":"POOCHIES","email":"bernadettemann@poochies.com","phone":"+1 (830) 508-3911","address":"208 Garden Street, Selma, Puerto Rico, 9739","registered":"2018-04-07T04:56:06 -07:00","latitude":-20.732629,"longitude":-87.665746,"tags":["elit","culpa","laboris","incididunt","amet","deserunt","eu"],"friends":[{"id":0,"name":"Holcomb Graves"},{"id":1,"name":"Elba Peterson"},{"id":2,"name":"Jones Franco"}],"greeting":"Hello, Bernadette Mann! You have 2 unread messages.","favoriteFruit":"banana"}
{"index":{"_index":"employees","_type":"doc"}}
{"id":"5b2b57c4504f5f81f69074bd","index":11,"guid":"a1ee11e6-d4e1-4aad-9e61-8888a6c5adee","isActive":false,"balance":"$2,195.29","picture":"http://placehold.it/32x32","age":36,"eyeColor":"blue","name":"Sharpe Small","gender":"male","company":"ECOSYS","email":"sharpesmall@ecosys.com","phone":"+1 (946) 581-2267","address":"652 Bulwer Place, Lemoyne, Pennsylvania, 4657","registered":"2014-04-12T11:54:15 -07:00","latitude":-70.587685,"longitude":-41.301646,"tags":["amet","deserunt","ad","ex","aute","consequat","sit"],"friends":[{"id":0,"name":"Brady Barker"},{"id":1,"name":"Terra Velez"},{"id":2,"name":"Jacquelyn Merritt"}],"greeting":"Hello, Sharpe Small! You have 1 unread messages.","favoriteFruit":"banana"}

# Basic match
GET employees/_search
{
  "query": {
    "match": {
      "eyeColor": "blue"
    }
  }
}

# Match relevant
GET /employees/_search
{
  "query": {
    "match": {
      "friends.name": "sophia larsen"
    }
  }
}

# Match phrase
GET employees/_search
{
  "query": {
    "match_phrase": {
      "friends.name": "sophia larsen"
    }
  }
}

# Match AND & OR
GET employees/_search
{
  "query": {
    "bool": {
      "must": [
        {
          "match": {
            "eyeColor": "blue"
          }
        },
        {
          "match": {
            "gender": "female"
          }
        }
      ]
    }
  }
}
GET employees/_search
{
  "query": {
    "bool": {
      "should": [
        {
          "match": {
            "eyeColor": {
              "query": "blue",
              "boost": 3
            }
          }
        },
        {
          "match": {
            "gender": "male"
          }
        }
      ]
    }
  }
}

# Highlight
GET employees/_search
{
  "query": {
    "match_phrase": {
      "friends.name": "larsen"
    }
  },
  "highlight": {
    "fields": {
      "friends.name": {}
    }
  }
}

# Match range
GET employees/_search
{
  "query": {
    "range": {
      "age": {
        "gte": 20,
        "lte": 23
      }
    }
  },
  "sort": [
    {
      "age": {
        "order": "asc"
      }
    }
  ]
}

# Aggregation
GET employees/_search
{
  "query": {
    "match_all": {}
  },
  "aggs": {
    "age_range": {
      "range": {
        "field": "age",
        "ranges": [
          {
            "key": "18-25",
            "from": 18,
            "to": 25
          },
          {
            "key": "26-30",
            "from": 26,
            "to": 30
          },
          {
            "key": "31-40",
            "from": 31,
            "to": 40
          }
        ]
      }
    }
  }
}

# Mapping
GET employees/_mapping
PUT employees/_mapping/doc
{
  "properties": {
    "address": {
      "type": "keyword"
    },
    "age": {
      "type": "long"
    },
    "balance": {
      "type": "keyword"
    },
    "company": {
      "type": "keyword"
    },
    "email": {
      "type": "keyword"
    },
    "eyeColor": {
      "type": "keyword"
    },
    "favoriteFruit": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword",
          "ignore_above": 256
        }
      }
    },
    "friends": {
      "properties": {
        "id": {
          "type": "keyword"
        },
        "name": {
          "type": "text",
          "fields": {
            "keyword": {
              "type": "keyword",
              "ignore_above": 256
            }
          }
        }
      }
    },
    "gender": {
      "type": "keyword"
    },
    "greeting": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword",
          "ignore_above": 256
        }
      }
    },
    "guid": {
      "type": "keyword"
    },
    "id": {
      "type": "keyword"
    },
    "index": {
      "type": "long"
    },
    "isActive": {
      "type": "boolean"
    },
    "latitude": {
      "type": "float"
    },
    "longitude": {
      "type": "float"
    },
    "name": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword",
          "ignore_above": 256
        }
      }
    },
    "phone": {
      "type": "keyword"
    },
    "picture": {
      "type": "keyword"
    },
    "registered": {
      "type": "keyword"
    },
    "tags": {
      "type": "keyword"
    }
  }
}

# Delete Document
GET employees/doc/1234
DELETE employees/doc/1234
