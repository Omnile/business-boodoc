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

Here's the complete documentaiton of the avialable API Endpoints.
[Get Postman Collection](http://business.booconnect.run/docs/business/collection.json)

# User Authentication

## Api Token

BooConnect’s authentication is via the “Authorization” header, which allows the caller to specify an access token.

Access tokens are used to maintain a session and are created via the password login or Oauth login paths. Typical access tokens are valid for 24 hours. After expiry the user must re-authenticate.

The BooConnect server expects for the API key to be included in all API requests to the server in a header that looks like the following:

-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a..."

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/**" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a..."
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/**",
    "method": "GET|POST|PUT|DELETE",
    "data": {

	},
    "headers": {
        "accept": "application/json",
        "Authentication": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a..."
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request

`POST api/b/v1/**`


## Login

Get a token for to the BooConnect API. This is only intended for users accessing their own accounts.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/**" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a..." \
    -d "username"="colt.ratke" \
    -d "password"="google" \
    -d "client_id"="mobile_app" \
    -d "client_secret"="PjHwDguIpGkEy15b1JBaBToMp2bb3DJfeaUrH8Q3" \
    -d "grant_type"="password" \
    -d "scope"="*" \
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/**",
    "method": "POST",
    "data": {
        "username":"colt.ratke",
        "password":"google",
        "client_id":"mobile_app",
        "client_secret":"PjHwDguIpGkEy15b1JBaBToMp2bb3DJfeaUrH8Q3",
        "grant_type":"password",
        "scope":"*"
    },
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
{
    "token_type":"Bearer",
    "expires_in":31536000,
    "access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a...",
    "refresh_token":"def50200b140f70041e75ac7666c580b08fde49d..."
}
```

### HTTP Request

`POST api/oauth/token`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    username | string | required |  The username of the user
    password | string | required |  The password of the user
    client_id | string | required | The OAuth Client ID
    client_secret | string | required | The OAuth Client Secret
    grant_type | string | required | `password`
    scope | string | required | `*`



## Register User Restaurant Account

When registering a restaurant account, it creates both a user and the restaurant profile. This user account can ba used to login as a customer or on the business system as a business owner.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/**" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a..." \
    -d "gender"="male" \
    -d "lastname"="Ariama" \
    -d "password"="google" \
    -d "username"="ovac4uss" \
    -d "restaurant_name"="ovac restaurant" \
    -d "firstname"="Victor" \
    -d "phone"="055357726112" \
    -d "registration_no"="123" \
    -d "password_confirmation"="google" \
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/**",
    "method": "POST",
    "data": {
        "gender": "male",
        "lastname": "Ariama",
        "password": "google",
        "username": "ovac4uss",
        "restaurant_name": "ovac restaurant",
        "firstname": "Victor",
        "phone": "055357726112",
        "registration_no": "123",
        "password_confirmation": "google"
    },
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
{
    "firstname": "Victor",
    "lastname": "Ariama",
    "username": "ovac4uss",
    "gender": "male",
    "phone": "055357726112",
    "updated_at": "2018-03-23 02:57:58",
    "created_at": "2018-03-23 02:57:58",
    "id": 3,
    "restaurant_id": 3,
    "name": "Victor Ariama",
    "restaurant": {
        "id": 3,
        "name": "ovac restaurant",
        "phone": "055357726112",
        "registration_no": "123",
        "owner_id": "3",
        "image": "/images/restaurant_default_image.svg",
        "cover": "/images/restaurant_default_cover.svg",
        "place": null,
        "city": null,
        "state": null,
        "country": null,
        "address": null,
        "website": null,
        "description": null,
        "phone_verified": 0,
        "email_verified": 0,
        "deleted_at": null,
        "created_at": "2018-03-23 02:57:58",
        "updated_at": "2018-03-23 02:57:58"
    }
}
```

### HTTP Request

`POST api/oauth/token`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    firstname | string | required | The first name of the user
    lastname | string | required | The last name of the user
    gender | string | retuired | The gender of the user `male` or `female`,
    username | string | required |  The username of the user
    password | string | required |  The password of the use
    password_confirmation | string | required | A confirmation of the password
    restaurant_name | string | required | The name of the restaurant to register
    phone | string | required | This will be the number for the user and restaurant.
    registration_no | integer | required | This is the business registration number


## Register User Customer Account

Register a customer account.

> Example request:

```bash
curl -X POST "http://booconnect.run/api/v1/**" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0a..." \
    -d "gender"="male" \
    -d "lastname"="Ariama" \
    -d "password"="google" \
    -d "username"="ovac4uss" \
    -d "firstname"="Victor" \
    -d "phone"="055357726112" \
    -d "password_confirmation"="google" \
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/**",
    "method": "POST",
    "data": {
        "gender": "male",
        "lastname": "Ariama",
        "password": "google",
        "username": "ovac4uss",
        "firstname": "Victor",
        "phone": "055357726112",
        "password_confirmation": "google"
    },
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
{
    "firstname": "Victor",
    "lastname": "Ariama",
    "username": "ovac4uss",
    "gender": "male",
    "phone": "055357726112",
    "updated_at": "2018-03-23 02:57:58",
    "created_at": "2018-03-23 02:57:58",
    "id": 3,
    "restaurant_id": 3,
    "name": "Victor Ariama"
}
```

### HTTP Request

`POST api/oauth/token`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    firstname | string | required | The first name of the user
    lastname | string | required | The last name of the user
    gender | string | retuired | The gender of the user `male` or `female`,
    username | string | required |  The username of the user
    password | string | required |  The password of the use
    password_confirmation | string | required | A confirmation of the password
    phone | string | required | This will be the number for the user and restaurant.
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
{
    "id": 1,
    "firstname": "Enoch",
    "lastname": "Stroman",
    "username": "elijah37",
    "phone": "790.894.7383",
    "gender": "female",
    "restaurant_id": 1,
    "phone_verified": 1,
    "email_verified": 1,
    "deleted_at": null,
    "created_at": "2018-03-23 17:33:11",
    "updated_at": "2018-03-23 17:33:11",
    "name": "Enoch Stroman"
}
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
{
    "current_page": 1,
    "data": [
        {
            "id": 1,
            "quantity": 9,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "transit",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "restaurant_id": 1,
            "formatted_price": "GHC 1.00"
        },
        {
            "id": 3,
            "quantity": 4,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "transit",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "restaurant_id": 1,
            "formatted_price": "GHC 1.00"
        },
        {
            "id": 4,
            "quantity": 4,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "transit",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "restaurant_id": 1,
            "formatted_price": "GHC 1.00"
        }
    ],
    "first_page_url": "http:\/\/localhost\/api\/b\/v1\/completed-orders?page=1",
    "from": 1,
    "last_page": 1,
    "last_page_url": "http:\/\/localhost\/api\/b\/v1\/completed-orders?page=1",
    "next_page_url": null,
    "path": "http:\/\/localhost\/api\/b\/v1\/completed-orders",
    "per_page": 20,
    "prev_page_url": null,
    "to": 3,
    "total": 3
}
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
{
    "id": 1,
    "quantity": 9,
    "price": "1",
    "item_id": 1,
    "user_id": 1,
    "status": "transit",
    "created_at": "2018-03-23 17:33:12",
    "updated_at": "2018-03-23 17:33:12",
    "formatted_price": "GHC 1.00"
}
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
{
    "current_page": 1,
    "data": [
        {
            "id": 1,
            "name": "RIce & beans",
            "restaurant_id": 1,
            "image": "https:\/\/lorempixel.com\/150\/150\/food\/?71002",
            "description": "Ut corporis omnis quia reiciendis eveniet laudantium maxime.",
            "price": 1,
            "user_id": 1,
            "measurement": "plate",
            "quantity": 2,
            "deleted_at": null,
            "created_at": "2018-03-23 17:33:11",
            "updated_at": "2018-03-23 17:33:11",
            "formatted_price": "GHC 1.00",
            "cart": [],
            "qty": 0,
            "in_cart": false
        },
        {
            "id": 2,
            "name": "Akeem",
            "restaurant_id": 1,
            "image": "https:\/\/lorempixel.com\/150\/150\/food\/?71002",
            "description": "Ut corporis omnis quia reiciendis eveniet laudantium maxime.",
            "price": 1,
            "user_id": 1,
            "measurement": "plate",
            "quantity": 2,
            "deleted_at": null,
            "created_at": "2018-03-23 17:33:11",
            "updated_at": "2018-03-23 17:33:11",
            "formatted_price": "GHC 1.00",
            "cart": [],
            "qty": 0,
            "in_cart": false
        }
    ],
    "first_page_url": "http:\/\/localhost\/api\/b\/v1\/items?page=1",
    "from": 1,
    "last_page": 1,
    "last_page_url": "http:\/\/localhost\/api\/b\/v1\/items?page=1",
    "next_page_url": null,
    "path": "http:\/\/localhost\/api\/b\/v1\/items",
    "per_page": 20,
    "prev_page_url": null,
    "to": 2,
    "total": 2
}
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
{
    "id": 1,
    "name": "RIce & beans",
    "restaurant_id": 1,
    "image": "https:\/\/lorempixel.com\/150\/150\/food\/?71002",
    "description": "Ut corporis omnis quia reiciendis eveniet laudantium maxime.",
    "price": 1,
    "user_id": 1,
    "measurement": "plate",
    "quantity": 2,
    "deleted_at": null,
    "created_at": "2018-03-23 17:33:11",
    "updated_at": "2018-03-23 17:33:11",
    "formatted_price": "GHC 1.00",
    "cart": [],
    "qty": 0,
    "in_cart": false,
    "rating": [],
    "orders": [
        {
            "id": 1,
            "quantity": 9,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "transit",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "formatted_price": "GHC 1.00"
        },
        {
            "id": 2,
            "quantity": 4,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "pending",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "formatted_price": "GHC 1.00"
        },
        {
            "id": 3,
            "quantity": 4,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "transit",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "formatted_price": "GHC 1.00"
        },
        {
            "id": 4,
            "quantity": 4,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "transit",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "formatted_price": "GHC 1.00"
        }
    ],
    "pictures": {
        "id": 1,
        "imageable_id": 1,
        "path": "https:\/\/lorempixel.com\/150\/150\/food\/?66415",
        "description": "THE VOICE OF THE.",
        "imageable_type": "App\\Item",
        "created_at": "2018-03-23 17:33:12",
        "updated_at": "2018-03-23 17:33:12"
    },
    "wishlist": []
}
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

> Example response:

```json
"{}"
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
{
    "current_page": 1,
    "data": [
        {
            "id": 2,
            "quantity": 4,
            "price": "1",
            "item_id": 1,
            "user_id": 1,
            "status": "pending",
            "created_at": "2018-03-23 17:33:12",
            "updated_at": "2018-03-23 17:33:12",
            "restaurant_id": 1,
            "formatted_price": "GHC 1.00"
        }
    ],
    "first_page_url": "http:\/\/localhost\/api\/b\/v1\/pending-orders?page=1",
    "from": 1,
    "last_page": 1,
    "last_page_url": "http:\/\/localhost\/api\/b\/v1\/pending-orders?page=1",
    "next_page_url": null,
    "path": "http:\/\/localhost\/api\/b\/v1\/pending-orders",
    "per_page": 20,
    "prev_page_url": null,
    "to": 1,
    "total": 1
}
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
{
    "id": 1,
    "quantity": 9,
    "price": "1",
    "item_id": 1,
    "user_id": 1,
    "status": "transit",
    "created_at": "2018-03-23 17:33:12",
    "updated_at": "2018-03-23 17:33:12",
    "formatted_price": "GHC 1.00"
}
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

> Example response:

```json
"{}"
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
{
    "id": 1,
    "name": "Sawayn-Smitham",
    "phone": "+1.820.682.4627",
    "registration_no": "61705",
    "owner_id": "1",
    "image": "https:\/\/lorempixel.com\/150\/150\/nightlife\/?32283",
    "cover": "https:\/\/lorempixel.com\/500\/150\/technics\/?48519",
    "place": "Riceborough",
    "city": "West Vivianneville",
    "state": "Arizona",
    "country": "Djibouti",
    "address": "3391 Parker Circle",
    "website": "hills.com",
    "description": "Perferendis eaque magni enim est optio est cumque.",
    "phone_verified": 0,
    "email_verified": 1,
    "deleted_at": null,
    "created_at": "2018-03-23 17:33:11",
    "updated_at": "2018-03-23 17:33:11"
}
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

