---
title: BooConnect API Reference

language_tabs:
- bash
- javascript

includes:
- errors

search: true

toc_footers:
- <a href="#">Some footer message comes here.</a>
---
<!-- START_INFO -->
# Info

Here's tsshe complete documentaiton of the avialable API Endpoints.
[Get Postman Collection](http://business.booconnect.run/docs/business/collection.json)

# Authentication

BooConnect uses API keys to allow access to the API.
A new api key will be granted when loed in and thereafter, the server will expect a stateless call with the api key set as an authorization bearer.

The BooConnect server expects for the API key to be included in all API requests to the server in a header that looks like the following:

Authorization: meowmeowmeow
<!-- END_INFO -->

#Account
Manage Resturant Admin Account
<!-- START_3842d14fd5cb8fe59c19b1ce358cd3c2 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/account" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/account`

`HEAD api/b/v1/account`


<!-- END_3842d14fd5cb8fe59c19b1ce358cd3c2 -->

<!-- START_c12cce6ee6bf8c705b01f452b66afe81 -->
## Update Account
Update the authenticated user account.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/account" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a" \
    -d "firstname"="cupiditate" \
    -d "lastname"="cupiditate" \
    -d "username"="cupiditate" \
    -d "gender"="cupiditate" \
    -d "phone"="cupiditate" \
    -d "password"="cupiditate" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account",
    "method": "POST",
    "data": {
        "firstname": "cupiditate",
        "lastname": "cupiditate",
        "username": "cupiditate",
        "gender": "cupiditate",
        "phone": "cupiditate",
        "password": "cupiditate"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`POST api/b/v1/account`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    firstname | string |  required  | Maximum: `255`
    lastname | string |  required  | Maximum: `255`
    username | string |  required  | Minimum: `4`
    gender | string |  required  | Minimum: `4`
    phone | string |  required  | Minimum: `4`
    password | string |  optional  | Minimum: `6`

<!-- END_c12cce6ee6bf8c705b01f452b66afe81 -->

#Completed Orders

View order history
<!-- START_59ca8e0853feceb1a413a6393eddd1b2 -->
## List Completed Orders
Display the order history list.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/completed-orders" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/completed-orders",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/completed-orders`

`HEAD api/b/v1/completed-orders`


<!-- END_59ca8e0853feceb1a413a6393eddd1b2 -->

<!-- START_37e95360e03ea7b92d1210070351bf39 -->
## Get completed order
Get a completed order form storage

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/completed-orders/{completed_order}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/completed-orders/{completed_order}",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/completed-orders/{completed_order}`

`HEAD api/b/v1/completed-orders/{completed_order}`


<!-- END_37e95360e03ea7b92d1210070351bf39 -->

#Items

Manage Items (Products)
<!-- START_e75e7766c4c2e8b61a42acc669ca71b5 -->
## Query All Items (Products)
Get a list of paginated items.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/items" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/items",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/items`

`HEAD api/b/v1/items`


<!-- END_e75e7766c4c2e8b61a42acc669ca71b5 -->

<!-- START_6e91d429fc36e8fe3e1e0e3b0bf06ce2 -->
## Create a new Item (Product)
Store a newly created Item in storage.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/items" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a" \
    -d "name"="sed" \
    -d "price"="1149859159" \
    -d "image"="sed" \
    -d "quantity"="1149859159" \
    -d "description"="sed" \
    -d "measurement"="sed" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/items",
    "method": "POST",
    "data": {
        "name": "sed",
        "price": 1149859159,
        "image": "sed",
        "quantity": 1149859159,
        "description": "sed",
        "measurement": "sed"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`POST api/b/v1/items`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    name | string |  required  | 
    price | numeric |  required  | Minimum: `1`
    image | image |  required  | Must be an image (jpeg, png, bmp, gif, or svg) Allowed mime types: `jpeg`, `jpg` or `png` Maximum: `1000`
    quantity | numeric |  required  | Minimum: `1`
    description | string |  required  | 
    measurement | string |  required  | 

<!-- END_6e91d429fc36e8fe3e1e0e3b0bf06ce2 -->

<!-- START_c3228e5219b9f997c157988318bdefbb -->
## Get Item
Get a single Item

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/items/{item}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/items/{item}",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/items/{item}`

`HEAD api/b/v1/items/{item}`


<!-- END_c3228e5219b9f997c157988318bdefbb -->

<!-- START_b138ef81d474838dd1693c310885c1ed -->
## Update Item
Update an item.

> Example request:

```bash
curl -X PUT "http://business.booconnect.run/api/b/v1/items/{item}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a" \
    -d "name"="officiis" \
    -d "price"="1875054879" \
    -d "image"="officiis" \
    -d "quantity"="1875054879" \
    -d "description"="officiis" \
    -d "measurement"="officiis" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/items/{item}",
    "method": "PUT",
    "data": {
        "name": "officiis",
        "price": 1875054879,
        "image": "officiis",
        "quantity": 1875054879,
        "description": "officiis",
        "measurement": "officiis"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`PUT api/b/v1/items/{item}`

`PATCH api/b/v1/items/{item}`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    name | string |  required  | 
    price | numeric |  required  | Minimum: `1`
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg) Allowed mime types: `jpeg`, `jpg` or `png` Maximum: `1000`
    quantity | numeric |  required  | Minimum: `1`
    description | string |  required  | 
    measurement | string |  required  | 

<!-- END_b138ef81d474838dd1693c310885c1ed -->

<!-- START_e3ec8b920d18e037be1cf325dd1c0ef2 -->
## Delete an Item
Remove an Item from the Items in this store.

> Example request:

```bash
curl -X DELETE "http://business.booconnect.run/api/b/v1/items/{item}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/items/{item}",
    "method": "DELETE",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`DELETE api/b/v1/items/{item}`


<!-- END_e3ec8b920d18e037be1cf325dd1c0ef2 -->

#Pending Orders
Manage pending orders
<!-- START_151b29795a3702c9c67c7c59d5993aa1 -->
## List Pending Orders
Query paginated list of pending orders.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/pending-orders" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/pending-orders",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/pending-orders`

`HEAD api/b/v1/pending-orders`


<!-- END_151b29795a3702c9c67c7c59d5993aa1 -->

<!-- START_57fd8a9aeb8e80bd442f5707a443f01d -->
## Display the specified resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/pending-orders/{pending_order}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/pending-orders/{pending_order}",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/pending-orders/{pending_order}`

`HEAD api/b/v1/pending-orders/{pending_order}`


<!-- END_57fd8a9aeb8e80bd442f5707a443f01d -->

<!-- START_72092d6ff54d537a07c074573d1a1ac9 -->
## Cancel Order
Cancel an order that was placed.

This option is only available within first 5 mins from time of order.

> Example request:

```bash
curl -X DELETE "http://business.booconnect.run/api/b/v1/pending-orders/{pending_order}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/pending-orders/{pending_order}",
    "method": "DELETE",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`DELETE api/b/v1/pending-orders/{pending_order}`


<!-- END_72092d6ff54d537a07c074573d1a1ac9 -->

#Restaurant Settings
Manage Resturant Settings
<!-- START_30fc43ff1dd77ce42b850b4fade37087 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/settings" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/settings",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/settings`

`HEAD api/b/v1/settings`


<!-- END_30fc43ff1dd77ce42b850b4fade37087 -->

<!-- START_71e3f45927a5c500892e3a5e61f75cb6 -->
## Update Business Settings.

Update the Business (restaurant) configurations

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/settings" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a" \
    -d "name"="ut" \
    -d "phone"="58019" \
    -d "registration_no"="58019" \
    -d "image"="ut" \
    -d "cover"="ut" \
    -d "place"="ut" \
    -d "city"="ut" \
    -d "state"="ut" \
    -d "country"="ut" \
    -d "address"="ut" \
    -d "website"="ut" \
    -d "description"="ut" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/settings",
    "method": "POST",
    "data": {
        "name": "ut",
        "phone": 58019,
        "registration_no": 58019,
        "image": "ut",
        "cover": "ut",
        "place": "ut",
        "city": "ut",
        "state": "ut",
        "country": "ut",
        "address": "ut",
        "website": "ut",
        "description": "ut"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`POST api/b/v1/settings`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    name | string |  optional  | 
    phone | numeric |  optional  | 
    registration_no | numeric |  optional  | 
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg) Allowed mime types: `jpeg`, `jpg` or `png` Maximum: `1000`
    cover | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg) Allowed mime types: `jpeg`, `jpg` or `png` Maximum: `1000`
    place | string |  optional  | 
    city | string |  optional  | 
    state | string |  optional  | 
    country | string |  optional  | 
    address | string |  optional  | 
    website | string |  optional  | 
    description | string |  optional  | 

<!-- END_71e3f45927a5c500892e3a5e61f75cb6 -->

#general
<!-- START_a75b7645bac3c852d0f819d20eeb8f02 -->
## Show the application&#039;s login form.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/login" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/login",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/login`

`HEAD api/b/v1/login`


<!-- END_a75b7645bac3c852d0f819d20eeb8f02 -->

<!-- START_c09f6cf14398682d96cb08debcf4c050 -->
## Show the application registration form.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/register" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/register",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/register`

`HEAD api/b/v1/register`


<!-- END_c09f6cf14398682d96cb08debcf4c050 -->

<!-- START_5058596eae09fe7bba75f0e245c95877 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/dashboard" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/dashboard`

`HEAD api/b/v1/dashboard`


<!-- END_5058596eae09fe7bba75f0e245c95877 -->

<!-- START_1d076070df5be1eeee0455066f397195 -->
## Show the form for creating a new resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/dashboard/create" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard/create",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/dashboard/create`

`HEAD api/b/v1/dashboard/create`


<!-- END_1d076070df5be1eeee0455066f397195 -->

<!-- START_9c41e628d73875080916a7cbef74f502 -->
## Store a newly created resource in storage.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/dashboard" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard",
    "method": "POST",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`POST api/b/v1/dashboard`


<!-- END_9c41e628d73875080916a7cbef74f502 -->

<!-- START_a73b35ab9f4ffded9c155bb79b6f7387 -->
## Display the specified resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/dashboard/{dashboard}`

`HEAD api/b/v1/dashboard/{dashboard}`


<!-- END_a73b35ab9f4ffded9c155bb79b6f7387 -->

<!-- START_e9d636af646e6750889f280e46f44b22 -->
## Show the form for editing the specified resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}/edit" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}/edit",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request

`GET api/b/v1/dashboard/{dashboard}/edit`

`HEAD api/b/v1/dashboard/{dashboard}/edit`


<!-- END_e9d636af646e6750889f280e46f44b22 -->

<!-- START_0cd42cdbb34018932e29527c04724a17 -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}",
    "method": "PUT",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`PUT api/b/v1/dashboard/{dashboard}`

`PATCH api/b/v1/dashboard/{dashboard}`


<!-- END_0cd42cdbb34018932e29527c04724a17 -->

<!-- START_4121ca3e6816c677f2c568dcfad49cff -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/dashboard/{dashboard}",
    "method": "DELETE",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`DELETE api/b/v1/dashboard/{dashboard}`


<!-- END_4121ca3e6816c677f2c568dcfad49cff -->

