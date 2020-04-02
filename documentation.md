
# CI-BackEnd

This collection contains all API resuests from CI-backend.

## Indices

* [users](#users)

  * [users/sso](#1-userssso)
  * [users/:fornova_id/rooms](#2-users:fornova_idrooms)
  * [users/compsets](#3-userscompsets)

* [supported](#supported)

  * [supported/providers](#1-supportedproviders)
  * [supported/meal-types](#2-supportedmeal-types)
  * [supported/los](#3-supportedlos)
  * [supported/price-filters](#4-supportedprice-filters)

* [compsets](#compsets)

  * [compsets/:fornova_id](#1-compsets:fornova_id)
  * [compsets/:id/rooms](#2-compsets:idrooms)
  * [compsets/rooms](#3-compsetsrooms)
  * [compsets/create](#4-compsetscreate)

* [rooms](#rooms)

  * [rooms](#1-rooms)

* [market](#market)

  * [market/:compset_id/:year/:month/:provider_name/:los/:pos](#1-market:compset_id:year:month:provider_name:los:pos)
  * [market/single-date-trend/:day/:group_doc_id](#2-marketsingle-date-trend:day:group_doc_id)
  * [market/compset/:id/customer-review'](#3-marketcompset:idcustomer-review')

* [rate](#rate)

  * [rate/compset_id/:year/:month/:provider_name/:los/:pos (GET)](#1-ratecompset_id:year:month:provider_name:los:pos-(get))
  * [rate/single-date-trend/:day/:group_doc_id](#2-ratesingle-date-trend:day:group_doc_id)


--------


## users
user/sso



### 1. users/sso


Retrun user info


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{API-URL}}/users/sso
```



***Body:***

```js        
{
	"token":"U2FsdGVkX19OFRSisi9LTSr9GVVpvFapuF+s1JUU/fcOsLARBoLaNtIXOzbkmMqDMueYwuRM27hTH32MndUnTyn5LOooYoj4VTX+2Yi855uFZGqvLdKCBKri+gRHX4DjToiWX5MsjEMQJcJvISNzOfR7t0CrPfkGnwuc5MNEULvPPIcJz2/k+yPy+mIlLTnaqr6nUFA0xBmNXcZJFm/VmV9UamTQf2wE97D9xIHE4eulncmKUt1nJvtdNTEhWKWYOoNwyNiPOGmhvjl3cDUhlztnUJdW6KmZDW2PFDa0Mw+MARF36XtIu0XPy7Dil/Hh"
}
```



***Responses:***


Status: users/sso | Code: 201



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 465 |
| ETag | W/"1d1-zWhOUUGkgj/tCP4G8Bh+8BozEJQ" |
| Date | Wed, 01 Apr 2020 07:37:05 GMT |
| Connection | keep-alive |



```js
{
    "fornova_user_id": "C21cQ6VjfUzwKDfga",
    "firstName": "",
    "lastName": "",
    "email": "",
    "level": "",
    "chainName": "",
    "chainId": "",
    "fornovaIds": [],
    "token": "U2FsdGVkX19OFRSisi9LTSr9GVVpvFapuF+s1JUU/fcOsLARBoLaNtIXOzbkmMqDMueYwuRM27hTH32MndUnTyn5LOooYoj4VTX+2Yi855uFZGqvLdKCBKri+gRHX4DjToiWX5MsjEMQJcJvISNzOfR7t0CrPfkGnwuc5MNEULvPPIcJz2/k+yPy+mIlLTnaqr6nUFA0xBmNXcZJFm/VmV9UamTQf2wE97D9xIHE4eulncmKUt1nJvtdNTEhWKWYOoNwyNiPOGmhvjl3cDUhlztnUJdW6KmZDW2PFDa0Mw+MARF36XtIu0XPy7Dil/Hh"
}
```



### 2. users/:fornova_id/rooms


Get my rooms types                                                params:                                                          
fornova_id: number                                                



***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/users/564607/rooms
```



***Responses:***


Status: users/rooms/:fornova_id | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 167 |
| ETag | W/"a7-LqVvsAuasEsCiCR32R2gIaTgmjs" |
| Date | Wed, 01 Apr 2020 09:12:06 GMT |
| Connection | keep-alive |



```js
{
    "Superiorrum": 2,
    "Premiumrum Scandinavian Style": 2,
    "Standardrum": 2,
    "Superiorrum Runway View": 2,
    "Superiorrum Terminal View": 2,
    "Familjerum": 2,
    "Juniorsvit Runway View": 2
}
```



### 3. users/compsets


return all compset,mealtypes and hotels name


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/users/compsets
```



***Responses:***


Status: users/compsets | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 1383 |
| ETag | W/"567-6OmZxT7mLIpVHkYIQpcny7vGWxU" |
| Date | Thu, 02 Apr 2020 14:21:22 GMT |
| Connection | keep-alive |



```js
{
    "compSet": [
        {
            "pos": [
                "SE",
                "DK",
                "FI",
                "NO",
                "US",
                "UK",
                "DE"
            ],
            "providers": [
                "booking",
                "expedia"
            ],
            "competitors": [
                523352,
                10824,
                523353
            ],
            "los": [
                1,
                2,
                3
            ],
            "_id": "5e85bf214794981e9ce28897",
            "name": "low",
            "type": "low",
            "customer_hotel_fornova_id": 32102,
            "customer_id": "nordic Choice",
            "customer_name": "Nordic Choice",
            "marketId": 27466,
            "main_pos": "US",
            "daily_scans": 30,
            "weekily_scans": 90,
            "on_demand": false,
            "__v": 0
        },
        {
            "pos": [
                "SE",
                "DK",
                "FI",
                "NO",
                "US",
                "UK",
                "DE"
            ],
            "providers": [
                "booking",
                "expedia"
            ],
            "competitors": [
                564607,
                564607
            ],
            "los": [
                1,
                2,
                3
            ],
            "_id": "5e85bf444794981e9ce28898",
            "name": "low",
            "type": "low",
            "customer_hotel_fornova_id": 32102,
            "customer_id": "nordic Choice",
            "customer_name": "Nordic Choice",
            "marketId": 27466,
            "main_pos": "US",
            "daily_scans": 30,
            "weekily_scans": 90,
            "on_demand": false,
            "__v": 0
        }
    ],
    "mealtypes": [
        {
            "_id": 0,
            "display_name": "Room Only",
            "name": "room_only"
        },
        {
            "_id": 1,
            "display_name": "Bed and breakfast",
            "name": "bnb"
        },
        {
            "_id": 2,
            "display_name": "Half Board",
            "name": "half_board"
        },
        {
            "_id": 3,
            "display_name": "Full Board",
            "name": "full_board"
        },
        {
            "_id": 5,
            "display_name": "All Inclusive",
            "name": "all_inclusive"
        }
    ],
    "hotels": [
        {
            "fornovaId": 10824,
            "hotel_name": "Radisson Blu Arlandia Hotel"
        },
        {
            "fornovaId": 523352,
            "hotel_name": "Best Western Arlanda Hotellby"
        },
        {
            "fornovaId": 523353,
            "hotel_name": "Best Western Plus Park Airport Hotel"
        },
        {
            "fornovaId": 564607,
            "hotel_name": "Radisson Blu Airport Terminal Hotel StockholmArlanda Airport"
        }
    ]
}
```



## supported
**supported**
*supported/providers(GET)
*supported/meal-types(GET)
*supported/los(GET)
*supported/price-filters(GET)



### 1. supported/providers


Get all providers 


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/supported/providers
```



***Responses:***


Status: supported/providers | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 123 |
| ETag | W/"7b-ZXCnoMe7w3i1RXcPaoX6NCGOKZ4" |
| Date | Wed, 01 Apr 2020 07:19:55 GMT |
| Connection | keep-alive |



```js
[
    {
        "_id": "5e04d22163d7ce10e85a0ac9",
        "provider_name": "Booking"
    },
    {
        "_id": "5e82fed0f811563d80a889c7",
        "provider_name": "expedia"
    }
]
```



### 2. supported/meal-types


Get all meal-types


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/supported/meal-types
```



***Responses:***


Status: supported/meal-types | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 295 |
| ETag | W/"127-JJKG27FL57wNOmmNTB2Y1cS2ojA" |
| Date | Wed, 01 Apr 2020 07:21:30 GMT |
| Connection | keep-alive |



```js
[
    {
        "_id": 0,
        "display_name": "Room Only",
        "name": "room_only"
    },
    {
        "_id": 1,
        "display_name": "Bed and breakfast",
        "name": "bnb"
    },
    {
        "_id": 2,
        "display_name": "Half Board",
        "name": "half_board"
    },
    {
        "_id": 3,
        "display_name": "Full Board",
        "name": "full_board"
    },
    {
        "_id": 5,
        "display_name": "All Inclusive",
        "name": "all_inclusive"
    }
]
```



### 3. supported/los


Get all los


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/supported/los
```



***Responses:***


Status: supported/los | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 24 |
| ETag | W/"18-dQ4ynCNaycOReSuiwQ0BGGiVSyQ" |
| Date | Wed, 01 Apr 2020 07:24:23 GMT |
| Connection | keep-alive |



```js
[
    {
        "_id": 1,
        "los_name": 1
    }
]
```



### 4. supported/price-filters


Get all price-filters


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/supported/price-filters
```



***Responses:***


Status: supported/price-filters | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 221 |
| ETag | W/"dd-sNBdN0k6HiBLcFt2DNJVTbibbjQ" |
| Date | Wed, 01 Apr 2020 07:26:52 GMT |
| Connection | keep-alive |



```js
[
    {
        "_id": "5e78cc2aa75e2f28b0143b02",
        "type": "3rd party Rates"
    },
    {
        "_id": "5e78cc2aa75e2f28b0143b03",
        "type": "Lowest"
    },
    {
        "_id": "5e78cc2aa75e2f28b0143b04",
        "type": "Best Flex"
    },
    {
        "_id": "5e78cc2aa75e2f28b0143b05",
        "type": "Fully Flex"
    }
]
```



## compsets
**compsets**
compsets/:fornova_id(GET)
compsets/:id/rooms(GET)
compsets/rooms(PUT)



### 1. compsets/:fornova_id


Get compset by fornova_id                                       
params:                                                         
fornova_id :number


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/compsets/11671
```



***Responses:***


Status: compsets/:fornova_id | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 3327 |
| ETag | W/"cff-p19G1h/g+2A6KwNY8TyyFPRxAYI" |
| Date | Wed, 01 Apr 2020 07:38:01 GMT |
| Connection | keep-alive |



```js
[
    {
        "providers": [
            "5e04d22163d7ce10e85a0ac9"
        ],
        "competitors_hotel_ids": [
            5232934,
            36450236,
            411524,
            5232934,
            10824,
            564607,
            523352,
            4899814,
            22954,
            523353,
            203731
        ],
        "_id": "5e7b32c7c2819a3b8cddda2e",
        "compset_type": "MEDIAN",
        "customer_hotel_id": 11671,
        "customer_id": "5e04975c0cf9f60768cc94eb",
        "los": 1,
        "marketId": 11673,
        "pos": "SE",
        "room_mapping": {
            "7886": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "8201": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "2 Queen Beds Nonsmoking Semiflex": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "15475": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "15823": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "42835": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "203731": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            }
        }
    },
    {
        "providers": [
            "5e04d22163d7ce10e85a0ac9"
        ],
        "competitors_hotel_ids": [
            42374087,
            45628620,
            30679558,
            907347,
            1436,
            33248297,
            33252641,
            22091618,
            41445832,
            37948727,
            3920234
        ],
        "_id": "5e7b4c40c2819a3b8cddda2f",
        "compset_type": "MEDIAN",
        "customer_hotel_id": 11671,
        "customer_id": "5e04975c0cf9f60768cc94eb",
        "los": 1,
        "marketId": 11673,
        "pos": "SE",
        "room_mapping": {
            "7886": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "8201": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "2 Queen Beds Nonsmoking Semiflex": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "15475": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "15823": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "42835": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            },
            "203731": {
                "my Budget Room": "Budget Room",
                "my Single Room": "Single Room",
                "my Standard level": "Standard level",
                "my Premium level": "Premium level",
                "my Suite": "Suite",
                "Family room": "Family room",
                "My Apartment": "Apartment"
            }
        }
    }
]
```



### 2. compsets/:id/rooms


Get compset room mapping                                        
params:                                                         
compset_id:string                                               


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/compsets/5e4d5ceb024c86101cf401d7/rooms
```



***Responses:***


Status: compsets/:id/rooms | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 32 |
| ETag | W/"20-TBlSASrOPvrCxIzNAvIuCKgIWbo" |
| Date | Wed, 01 Apr 2020 07:47:54 GMT |
| Connection | keep-alive |



```js
{
    "error": "No Relevent CompSet "
}
```



### 3. compsets/rooms


Update compset room mapping:                                    
body:                                                           
{
"compset_id":"",
"fornova_id":"",
"rooms":{"key":"value"}
}


***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{API-URL}}/compsets/rooms
```



***Body:***

```js        
{
"compset_id":"5e7b32c7c2819a3b8cddda2e",
"fornova_id":"8201",
"rooms":{"my Standard":"shaheen"}
}
```



***Responses:***


Status: compsets/rooms | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 1448 |
| ETag | W/"5a8-oFzmOSgDpehzW07Po9JGg8uUmTs" |
| Date | Wed, 01 Apr 2020 07:50:27 GMT |
| Connection | keep-alive |



```js
{
    "providers": [
        "5e04d22163d7ce10e85a0ac9"
    ],
    "competitors_hotel_ids": [
        5232934,
        36450236,
        411524,
        5232934,
        10824,
        564607,
        523352,
        4899814,
        22954,
        523353,
        203731
    ],
    "_id": "5e7b32c7c2819a3b8cddda2e",
    "compset_type": "MEDIAN",
    "customer_hotel_id": 11671,
    "customer_id": "5e04975c0cf9f60768cc94eb",
    "los": 1,
    "marketId": 11673,
    "pos": "SE",
    "room_mapping": {
        "7886": {
            "my Budget Room": "Budget Room",
            "my Single Room": "Single Room",
            "my Standard level": "Standard level",
            "my Premium level": "Premium level",
            "my Suite": "Suite",
            "Family room": "Family room",
            "My Apartment": "Apartment"
        },
        "8201": {
            "my Standard": "shaheen"
        },
        "15475": {
            "my Budget Room": "Budget Room",
            "my Single Room": "Single Room",
            "my Standard level": "Standard level",
            "my Premium level": "Premium level",
            "my Suite": "Suite",
            "Family room": "Family room",
            "My Apartment": "Apartment"
        },
        "15823": {
            "my Budget Room": "Budget Room",
            "my Single Room": "Single Room",
            "my Standard level": "Standard level",
            "my Premium level": "Premium level",
            "my Suite": "Suite",
            "Family room": "Family room",
            "My Apartment": "Apartment"
        },
        "42835": {
            "my Budget Room": "Budget Room",
            "my Single Room": "Single Room",
            "my Standard level": "Standard level",
            "my Premium level": "Premium level",
            "my Suite": "Suite",
            "Family room": "Family room",
            "My Apartment": "Apartment"
        },
        "203731": {
            "my Budget Room": "Budget Room",
            "my Single Room": "Single Room",
            "my Standard level": "Standard level",
            "my Premium level": "Premium level",
            "my Suite": "Suite",
            "Family room": "Family room",
            "My Apartment": "Apartment"
        }
    }
}
```



### 4. compsets/create


Create new compsets                                             
body:{                                                            
	customer_id:string,                                           
	name: string,                                                 
	type: string,                                               
	customer_name:string,                                       
	customer_hotel_fornova_id:number,                            
	pos:[string],                                               
	providers:[string],                                         
	competitors:[string],                                        
	competitors_name:object,                                       
	marketId:number,                                             
	los:[number],                                                
	main_pos:string,                                            
	daily_scans:number,                                         
	weekily_scans:number,                                       
	on_demand:boolean                                           
	 
}                                                


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{API-URL}}/compsets
```



***Body:***

```js        
{
"competitors": [
15475,
15823
],
"name":"low",
"type": "low",
"customer_hotel_fornova_id": 4256834567,
"customer_id": "nordic Choice",
"customer_name": "Nordic Choice",
"los": [1,2,3],
"marketId": 27466,
"pos": ["SE","DK","FI","NO","US","UK","DE"],
"providers": ["booking","expedia"],
"main_pos":"US",
"daily_scans":30,
"weekily_scans":90,
"on_demand":true
}
```



***Responses:***


Status: compsets/create | Code: 201



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 374 |
| ETag | W/"176-OQAXbCfpJTPeXr1wQbJXbkpZV48" |
| Date | Thu, 02 Apr 2020 11:32:06 GMT |
| Connection | keep-alive |



```js
{
    "pos": [
        "SE",
        "DK",
        "FI",
        "NO",
        "US",
        "UK",
        "DE"
    ],
    "providers": [
        "booking",
        "expedia"
    ],
    "competitors": [
        15475,
        15823
    ],
    "los": [
        1,
        2,
        3
    ],
    "_id": "5e85cd361fc84414b07d78cb",
    "name": "low",
    "type": "low",
    "customer_hotel_fornova_id": 4256834567,
    "customer_id": "nordic Choice",
    "customer_name": "Nordic Choice",
    "marketId": 27466,
    "main_pos": "US",
    "daily_scans": 30,
    "weekily_scans": 90,
    "on_demand": true,
    "__v": 0
}
```



## rooms
**rooms**
rooms (Get)



### 1. rooms


Get all rooms types


***Endpoint:***

```bash
Method: GET
Type: 
URL: 
```



***Responses:***


Status: rooms | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 723 |
| ETag | W/"2d3-0epPIWQr66U8lC2H1iPvsS1GNyQ" |
| Date | Wed, 01 Apr 2020 07:52:15 GMT |
| Connection | keep-alive |



```js
[
    {
        "indicators": [
            "budget",
            "basic"
        ],
        "_id": "5e3faf2eb4e3b0474c86ac20",
        "room_id": 7,
        "room_name": "Budget Room"
    },
    {
        "indicators": [
            "single"
        ],
        "_id": "5e3faf47b4e3b0474c86ac21",
        "room_id": 1,
        "room_name": "Single Room"
    },
    {
        "indicators": [
            "standard"
        ],
        "_id": "5e3faf5cb4e3b0474c86ac22",
        "room_id": 2,
        "room_name": "Standard level"
    },
    {
        "indicators": [
            "premium",
            "superior",
            "king",
            "deluxe"
        ],
        "_id": "5e3faf71b4e3b0474c86ac23",
        "room_id": 3,
        "room_name": "Premium level"
    },
    {
        "indicators": [
            "suite",
            "xxl"
        ],
        "_id": "5e3faf83b4e3b0474c86ac24",
        "room_id": 4,
        "room_name": "Suite"
    },
    {
        "indicators": [
            "family"
        ],
        "_id": "5e3faf91b4e3b0474c86ac25",
        "room_id": 5,
        "room_name": "Family room"
    },
    {
        "indicators": [
            "apartment"
        ],
        "_id": "5e3faf9fb4e3b0474c86ac26",
        "room_id": 6,
        "room_name": "Apartment"
    }
]
```



## market
**market**
market/compset_id/:year/:month/:provider_name/:los/:pos (GET)
market/compset/:id/customer-review (GET)
market/single-date-trend/:day/:group_doc_id (GET)



### 1. market/:compset_id/:year/:month/:provider_name/:los/:pos


Get compset group documents                                     
params:                                                          
compset_id:string-min(5)-max(50)                                 
year:number                                                     
month:number-min(1)-max(12)                                     
provider_name:string-min(5)-max(50)                                  
los:number-min(1)-max(10)                                       
pos:string


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/market/5e4d5ceb024c86101cf401d7/2020/3/booking/1/us
```



***Responses:***


Status: market/:compset_id/:year/:month/:provider_name/:los/:pos | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 2270 |
| ETag | W/"8de-v0q8rnKhZaRbhJ3nYHzoHI9bum4" |
| Date | Wed, 01 Apr 2020 07:55:01 GMT |
| Connection | keep-alive |



```js
{
    "_id": 8.826958726007918e+47,
    "checkin_dates": {
        "2": {
            "18213": {
                "position": 101
            },
            "18382": {
                "position": 152
            },
            "22736": {
                "position": 82
            },
            "1005890": {
                "position": 84
            },
            "4899814": {
                "position": 202
            }
        },
        "3": {
            "18002": {
                "position": 163
            },
            "18023": {
                "position": 36
            },
            "18213": {
                "position": 42
            },
            "18382": {
                "position": 143
            },
            "22736": {
                "position": 153
            },
            "4899814": {
                "position": 218
            }
        },
        "4": {
            "18002": {
                "position": 148
            },
            "18023": {
                "position": 34
            },
            "18213": {
                "position": 40
            },
            "18382": {
                "position": 126
            },
            "22736": {
                "position": 140
            },
            "1005890": {
                "position": 55
            }
        },
        "5": {
            "18002": {
                "position": 132
            },
            "18023": {
                "position": 54
            },
            "18213": {
                "position": 49
            },
            "22736": {
                "position": 149
            },
            "1005890": {
                "position": 85
            },
            "4899814": {
                "position": 208
            }
        },
        "8": {
            "18382": {
                "position": 192
            },
            "22736": {
                "position": 157
            },
            "1005890": {
                "position": 114
            },
            "4899814": {
                "position": 224
            }
        },
        "9": {
            "18023": {
                "position": 56
            },
            "1005890": {
                "position": 61
            },
            "4899814": {
                "position": 225
            }
        },
        "10": {
            "18023": {
                "position": 72
            },
            "18213": {
                "position": 62
            },
            "18382": {
                "position": 188
            },
            "1005890": {
                "position": 142
            },
            "4899814": {
                "position": 223
            }
        },
        "11": {
            "18002": {
                "position": 152
            },
            "18023": {
                "position": 24
            },
            "18213": {
                "position": 55
            },
            "18382": {
                "position": 188
            },
            "22736": {
                "position": 171
            },
            "1005890": {
                "position": 143
            },
            "4899814": {
                "position": 221
            }
        },
        "12": {
            "18002": {
                "position": 144
            },
            "18023": {
                "position": 41
            },
            "18213": {
                "position": 46
            },
            "22736": {
                "position": 112
            },
            "1005890": {
                "position": 84
            },
            "4899814": {
                "position": 205
            }
        },
        "13": {
            "18002": {
                "position": 120
            },
            "18023": {
                "position": 35
            },
            "18213": {
                "position": 56
            },
            "18382": {
                "position": 163
            },
            "22736": {
                "position": 9
            },
            "4899814": {
                "position": 200
            }
        },
        "14": {
            "18023": {
                "position": 65
            },
            "18382": {
                "position": 180
            },
            "22736": {
                "position": 146
            },
            "1005890": {
                "position": 118
            },
            "4899814": {
                "position": 216
            }
        },
        "21": {
            "18002": {
                "position": 170
            },
            "18023": {
                "position": 138
            },
            "18213": {
                "position": 172
            },
            "18382": {
                "position": 206
            },
            "22736": {
                "position": 103
            },
            "1005890": {
                "position": 178
            },
            "4899814": {
                "position": 232
            }
        },
        "27": {
            "18002": {
                "position": 170
            },
            "18023": {
                "position": 142
            },
            "18213": {
                "position": 176
            },
            "18382": {
                "position": 215
            },
            "22736": {
                "position": 95
            },
            "1005890": {
                "position": 191
            },
            "4899814": {
                "position": 241
            }
        },
        "30": {
            "18002": {
                "position": 160
            },
            "18023": {
                "position": 138
            },
            "18213": {
                "position": 172
            },
            "18382": {
                "position": 206
            },
            "22736": {
                "position": 83
            },
            "1005890": {
                "position": 184
            },
            "4899814": {
                "position": 236
            }
        }
    },
    "compset_id": "5e4d5ceb024c86101cf401d7",
    "los": 1,
    "month": 3,
    "pos": "us",
    "provider_name": "booking",
    "year": 2020
}
```



### 2. market/single-date-trend/:day/:group_doc_id


Get single date market                                          
params:                                                         
day:number-min(1)-max(31)                                       
group_doc_id:integer                                             


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/market/single-date-trend/2/1.1701471844438774e+48
```



***Responses:***


Status: market/single-date-trend/:day/:group_doc_id | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 357 |
| ETag | W/"165-zZWQMqIEQJqUebvEA2aI1LAwiQA" |
| Date | Wed, 01 Apr 2020 07:55:17 GMT |
| Connection | keep-alive |



```js
{
    "_id": "5e8322303c21626270b276df",
    "day": 2,
    "grouped_document_id": 1.1701471844438774e+48,
    "__v": 0,
    "trend_data": {
        "01-03-2020": {
            "10824": {
                "position": 15
            },
            "523353": {
                "position": 34
            },
            "564607": {
                "position": 17
            },
            "907347": {
                "position": 47
            },
            "3920234": {
                "position": 45
            },
            "30679558": {
                "position": 5
            },
            "33252641": {
                "position": 15
            },
            "36450236": {
                "position": 19
            },
            "42374087": {
                "position": 20
            }
        }
    }
}
```



### 3. market/compset/:id/customer-review'


Get compset customer review                                     
params:                                                         
compset_id:string


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/market/compset/5e7b32c7c2819a3b8cddda2e/customer-review
```



***Responses:***


Status: market/compset/:id/customer-review' | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 134 |
| ETag | W/"86-iIG4rwvtnOx241Fh1xZR8nj4IzU" |
| Date | Wed, 01 Apr 2020 07:56:05 GMT |
| Connection | keep-alive |



```js
{
    "booking": {
        "4899814": {
            "rating": 3,
            "total_reviwes": 0,
            "rating_improved": 0,
            "total_difference": 0,
            "hotelName": "Ramilton Old Town Hostel"
        }
    }
}
```



## rate
**rate**
rate/compset_id/:year/:month/:provider_name/:los/:pos (GET)
rate/single-date-trend/:day/:group_doc_id(GET)



### 1. rate/compset_id/:year/:month/:provider_name/:los/:pos (GET)


Get compset group documents (rate)                                 
params:                                                         
compset_id:string-min(5)-max(50)                                
year:number                                                     
month:number-min(1)-max(12)                                     
provider_name:string-min(5)-max(50)                             
los:number-min(1)-max(10)                                       
pos:string                                                      


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/rate/5e7b32c7c2819a3b8cddda2e/2020/4/expedia/1/SE
```



***Responses:***


Status: rate/compset_id/:year/:month/:provider_name/:los/:pos (GET) | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 44530 |
| ETag | W/"adf2-apGbcU6CU57cHNnUOzzSDzaX4l8" |
| Date | Wed, 01 Apr 2020 07:58:13 GMT |
| Connection | keep-alive |



```js
{
    "_id": 1.0543061970260315e+47,
    "checkin_dates": {
        "1": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4947,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9493,
                    "lowest": 4947
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4433,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2373
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6021,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13088,
                    "lowest": 6021
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 8552,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16533,
                    "lowest": 6513
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "2": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4723,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9320,
                    "lowest": 4723
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4392,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5957,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5013,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5909,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10496,
                    "lowest": 5909
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6037,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 8483,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14485,
                    "lowest": 6037
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5008,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6288,
                    "lowest": 5008
                }
            }
        },
        "3": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4114,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9320,
                    "lowest": 4114
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4163,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10085,
                    "lowest": 4984
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4481,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4481
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "4": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4114,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9320,
                    "lowest": 4114
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4163,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9856,
                    "lowest": 4984
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4481,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4481
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "5": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4114,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9540,
                    "lowest": 4114
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4392,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5250,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10565,
                    "lowest": 5250
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5525,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 6416,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13973,
                    "lowest": 5525
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "6": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4864,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9493,
                    "lowest": 4864
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4244,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2373
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5489,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9872,
                    "lowest": 5489
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6003,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14485,
                    "lowest": 6003
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5008,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6288,
                    "lowest": 5008
                }
            }
        },
        "7": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4947,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9529,
                    "lowest": 4947
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2373
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6021,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10053,
                    "lowest": 6021
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6037,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14485,
                    "lowest": 6037
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5008,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6288,
                    "lowest": 5008
                }
            }
        },
        "8": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4947,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9493,
                    "lowest": 4947
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4129,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2373
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6021,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10053,
                    "lowest": 6021
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5525,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 6416,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13973,
                    "lowest": 5525
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "9": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4185,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9320,
                    "lowest": 4185
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4163,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5957,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5013,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5521,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9525,
                    "lowest": 5521
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5494,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 6003,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13973,
                    "lowest": 5494
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "10": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4185,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9320,
                    "lowest": 4185
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4163,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10096,
                    "lowest": 4984
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4481,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4481
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "11": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4185,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9320,
                    "lowest": 4185
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4129,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10080,
                    "lowest": 4984
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4501,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 5252,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4501
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "12": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4185,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9493,
                    "lowest": 4185
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4163,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1800,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1800
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2200
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5250,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9792,
                    "lowest": 5250
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4481,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4481
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "13": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4226,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9493,
                    "lowest": 4226
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4129,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2373
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5489,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9525,
                    "lowest": 5489
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4501,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 5252,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4501
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "14": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4226,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9493,
                    "lowest": 4226
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4392,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2373
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6021,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9984,
                    "lowest": 6021
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5525,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 6416,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13973,
                    "lowest": 5525
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "15": {
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4433,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1877,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6037,
                    "lowest": 1877
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2118,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5189,
                    "lowest": 2118
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6021,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9984,
                    "lowest": 6021
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5749,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 6258,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14229,
                    "lowest": 5749
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "16": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4373
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4392,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1587,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5957,
                    "lowest": 1587
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5013,
                    "lowest": 2051
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5749,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13088,
                    "lowest": 5749
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6037,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 8483,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14485,
                    "lowest": 6037
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4752,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6032,
                    "lowest": 4752
                }
            }
        },
        "17": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4373
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4163,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1587,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1587
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2051
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9808,
                    "lowest": 5200
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4481,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4481
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "18": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4373
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 2449,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1587,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1587
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2051
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10053,
                    "lowest": 5200
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4481,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 4984,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4481
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "19": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4373,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4373
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4392,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1587,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1587
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2051
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5472,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 12421,
                    "lowest": 5472
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5525,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 6416,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13973,
                    "lowest": 5525
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "20": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4928,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4928
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4433,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1816,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6213,
                    "lowest": 1816
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 4118,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5701,
                    "lowest": 4118
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5765,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10016,
                    "lowest": 5765
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 8552,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16533,
                    "lowest": 6513
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "21": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 5013,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 5013
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 4192,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4969,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5472,
                    "lowest": 4192
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1889,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1889
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 4353,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5957,
                    "lowest": 4353
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6208,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10336,
                    "lowest": 6208
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 8304,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 8807,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16789,
                    "lowest": 8304
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "22": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 5013,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 5013
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 4192,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4929,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5472,
                    "lowest": 4192
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1889,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1889
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 4353,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5957,
                    "lowest": 4353
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6213,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10256,
                    "lowest": 6213
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 8341,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 9282,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16789,
                    "lowest": 8341
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "23": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4928,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4928
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 4192,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4969,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5472,
                    "lowest": 4192
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6469,
                    "lowest": 2051
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2419,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5525,
                    "lowest": 2419
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6405,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10512,
                    "lowest": 6405
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 8552,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16533,
                    "lowest": 6513
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "24": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4197,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4197
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1587,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1587
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2051
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9781,
                    "lowest": 5200
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4501,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4501
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "25": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4197,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4197
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 1888,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4129,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4704,
                    "lowest": 1888
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1587,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1587
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2051,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5445,
                    "lowest": 2051
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5200,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10320,
                    "lowest": 5200
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 4501,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 5252,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 13205,
                    "lowest": 4501
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 1936,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5008,
                    "lowest": 1936
                }
            }
        },
        "26": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4197,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4197
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1654,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6469,
                    "lowest": 1654
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 1889,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5269,
                    "lowest": 1889
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5477,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10560,
                    "lowest": 5477
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 5781,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14229,
                    "lowest": 5781
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 4496,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5776,
                    "lowest": 4496
                }
            }
        },
        "27": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4928,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4928
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4433,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1889,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1889
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 4353,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5957,
                    "lowest": 4353
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6208,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10608,
                    "lowest": 6208
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 8304,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 8807,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16789,
                    "lowest": 8304
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "28": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 5013,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 5013
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2400,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4660,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5216,
                    "lowest": 2400
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1889,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1889
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 4721,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6469,
                    "lowest": 4721
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6208,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 10528,
                    "lowest": 6208
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6549,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  1 dubbelsäng  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 9013,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16533,
                    "lowest": 6549
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "29": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 5013,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 5013
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2400,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4704,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5216,
                    "lowest": 2400
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1889,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6293,
                    "lowest": 1889
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 4721,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6469,
                    "lowest": 4721
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 6208,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9984,
                    "lowest": 6208
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 8552,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 16533,
                    "lowest": 6513
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5264,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6544,
                    "lowest": 5264
                }
            }
        },
        "30": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4928,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4928
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4433,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1816,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6213,
                    "lowest": 1816
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2184,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5269,
                    "lowest": 2184
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5749,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9573,
                    "lowest": 5749
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6003,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14485,
                    "lowest": 6003
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5008,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6288,
                    "lowest": 5008
                }
            }
        }
    },
    "compset_id": "5e7b32c7c2819a3b8cddda2e",
    "los": 1,
    "month": 4,
    "pos": "SE",
    "provider_name": "expedia",
    "year": 2020
}
```



### 2. rate/single-date-trend/:day/:group_doc_id


Get single date trend                                           
params:                                                         
day:number-min(1)-max(31)                                         
group_doc_id:integer                                                


***Endpoint:***

```bash
Method: GET
Type: 
URL: {{API-URL}}/rate/single-date-trend/30/1.0543061970260315e+47
```



***Responses:***


Status: rate/single-date-trend/:day/:group_doc_id | Code: 200



***Response Headers:***

| Key | Value |
| --- | ------|
| X-Powered-By | Express |
| Content-Type | application/json; charset=utf-8 |
| Content-Length | 1618 |
| ETag | W/"652-bGSPVT0Xpz7muoDLxmKBrzhWriM" |
| Date | Wed, 01 Apr 2020 07:58:29 GMT |
| Connection | keep-alive |



```js
{
    "_id": "5e842d813c21626270b66915",
    "day": 30,
    "grouped_document_id": 1.0543061970260315e+47,
    "__v": 0,
    "trend_data": {
        "25-03-2020": {
            "10824": {
                "rooms": {
                    "2": [
                        {
                            "price": 4928,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9605,
                    "lowest": 4928
                }
            },
            "411524": {
                "rooms": {
                    "2": [
                        {
                            "price": 2144,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standard dubbelrum  ickerökare"
                        }
                    ],
                    "3": [
                        {
                            "price": 4433,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 4960,
                    "lowest": 2144
                }
            },
            "523352": {
                "rooms": {
                    "2": [
                        {
                            "price": 1816,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6213,
                    "lowest": 1816
                }
            },
            "523353": {
                "rooms": {
                    "2": [
                        {
                            "price": 2184,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 5269,
                    "lowest": 2184
                }
            },
            "564607": {
                "rooms": {
                    "2": [
                        {
                            "price": 5749,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum"
                        }
                    ]
                },
                "statistics": {
                    "highest": 9573,
                    "lowest": 5749
                }
            },
            "5232934": {
                "rooms": {
                    "2": [
                        {
                            "price": 6003,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Standard"
                        }
                    ],
                    "3": [
                        {
                            "price": 6513,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Double Or Twin Superior"
                        }
                    ]
                },
                "statistics": {
                    "highest": 14485,
                    "lowest": 6003
                }
            },
            "36450236": {
                "rooms": {
                    "2": [
                        {
                            "price": 5008,
                            "occupancy": 2,
                            "cancellation": false,
                            "meal_type_id": 0,
                            "room_name": "Standardrum  2 enkelsängar  ickerökare"
                        }
                    ]
                },
                "statistics": {
                    "highest": 6288,
                    "lowest": 5008
                }
            }
        }
    }
}
```



---
[Back to top](#ci-backend)
> Made with &#9829; by [thedevsaddam](https://github.com/thedevsaddam) | Generated at: 2020-04-02 17:23:00 by [docgen](https://github.com/thedevsaddam/docgen)
