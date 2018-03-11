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
Manage Resturant Account
<!-- START_3842d14fd5cb8fe59c19b1ce358cd3c2 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/account" \
-H "Accept: application/json"
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/account`

`HEAD api/b/v1/account`


<!-- END_3842d14fd5cb8fe59c19b1ce358cd3c2 -->

<!-- START_b5f962e12b3ef2d8e27a9df0ed947d34 -->
## Show the form for creating a new resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/account/create" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account/create",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/account/create`

`HEAD api/b/v1/account/create`


<!-- END_b5f962e12b3ef2d8e27a9df0ed947d34 -->

<!-- START_c12cce6ee6bf8c705b01f452b66afe81 -->
## Store a newly created resource in storage.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/account" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account",
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

`POST api/b/v1/account`


<!-- END_c12cce6ee6bf8c705b01f452b66afe81 -->

<!-- START_9c9cdbc6c43979d197d5839976b2e28b -->
## Display the specified resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/account/{account}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account/{account}",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/account/{account}`

`HEAD api/b/v1/account/{account}`


<!-- END_9c9cdbc6c43979d197d5839976b2e28b -->

<!-- START_ae7fd50f797a1a371dfcc905143ec0c9 -->
## Show the form for editing the specified resource.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/account/{account}/edit" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account/{account}/edit",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/account/{account}/edit`

`HEAD api/b/v1/account/{account}/edit`


<!-- END_ae7fd50f797a1a371dfcc905143ec0c9 -->

<!-- START_842e6f96e2c98553048918966de02e72 -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT "http://business.booconnect.run/api/b/v1/account/{account}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account/{account}",
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

`PUT api/b/v1/account/{account}`

`PATCH api/b/v1/account/{account}`


<!-- END_842e6f96e2c98553048918966de02e72 -->

<!-- START_1d5088e4fdb1f4116f0b89c35961e147 -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE "http://business.booconnect.run/api/b/v1/account/{account}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/account/{account}",
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

`DELETE api/b/v1/account/{account}`


<!-- END_1d5088e4fdb1f4116f0b89c35961e147 -->

#Completed Orders

View order history
<!-- START_188002aaac5d541ffd7eb5c7b046154f -->
## List Completed Orders
Display the order history list.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/order" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/order",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/order`

`HEAD api/b/v1/order`


<!-- END_188002aaac5d541ffd7eb5c7b046154f -->

<!-- START_b2e1c8abc3c5ca79e02c4445245d9547 -->
## Get completed order
Get a completed order form storage

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/order/{order}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/order/{order}",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/order/{order}`

`HEAD api/b/v1/order/{order}`


<!-- END_b2e1c8abc3c5ca79e02c4445245d9547 -->

#Items

Manage Items (Products)
<!-- START_2a5220fa6c58f6a9b5152934814367e1 -->
## Query All Items (Products)
Get a list of paginated items.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/item" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/item",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/item`

`HEAD api/b/v1/item`


<!-- END_2a5220fa6c58f6a9b5152934814367e1 -->

<!-- START_9cfc669ca857653e99cea09706401e59 -->
## Create a new Item (Product)
Store a newly created Item in storage.

> Example request:

```bash
curl -X POST "http://business.booconnect.run/api/b/v1/item" \
-H "Accept: application/json" \
    -d "name"="et" \
    -d "price"="519947313" \
    -d "image"="et" \
    -d "quantity_daily"="519947313" \
    -d "measurement"="et" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/item",
    "method": "POST",
    "data": {
        "name": "et",
        "price": 519947313,
        "image": "et",
        "quantity_daily": 519947313,
        "measurement": "et"
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

`POST api/b/v1/item`


#### Parameters

Parameter | Type | Status | Description
---------|-------|-------|-------|-----------
    name | string |  required  | 
    price | numeric |  required  | Minimum: `1`
    image | image |  required  | Must be an image (jpeg, png, bmp, gif, or svg) Allowed mime types: `jpg` or `png` Maximum: `1000`
    quantity_daily | numeric |  required  | Minimum: `1`
    measurement | string |  required  | 

<!-- END_9cfc669ca857653e99cea09706401e59 -->

<!-- START_d8db387c7bbd64f7415284955d5b9741 -->
## Get Item
Get a single Item

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/item/{item}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/item/{item}",
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
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
```

### HTTP Request

`GET api/b/v1/item/{item}`

`HEAD api/b/v1/item/{item}`


<!-- END_d8db387c7bbd64f7415284955d5b9741 -->

<!-- START_b26a405220fe864661285e7d9f275e80 -->
## Update Item
Update an item.

> Example request:

```bash
curl -X PUT "http://business.booconnect.run/api/b/v1/item/{item}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/item/{item}",
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

`PUT api/b/v1/item/{item}`

`PATCH api/b/v1/item/{item}`


<!-- END_b26a405220fe864661285e7d9f275e80 -->

<!-- START_45ecdecd0bda444120ca8cff147949e8 -->
## Delete an Item
Remove an Item from the Items in this store.

> Example request:

```bash
curl -X DELETE "http://business.booconnect.run/api/b/v1/item/{item}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://business.booconnect.run/api/b/v1/item/{item}",
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

`DELETE api/b/v1/item/{item}`


<!-- END_45ecdecd0bda444120ca8cff147949e8 -->

#general
<!-- START_a75b7645bac3c852d0f819d20eeb8f02 -->
## Show the application&#039;s login form.

> Example request:

```bash
curl -X GET "http://business.booconnect.run/api/b/v1/login" \
-H "Accept: application/json"
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
{
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
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
-H "Accept: application/json"
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
{
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
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
-H "Accept: application/json"
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
{
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
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
-H "Accept: application/json"
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
{
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
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
-H "Accept: application/json"
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
-H "Accept: application/json"
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
{
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
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
-H "Accept: application/json"
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
{
    "message": "",
    "exception": "Symfony\\Component\\HttpKernel\\Exception\\NotFoundHttpException",
    "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/RouteCollection.php",
    "line": 179,
    "trace": [
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 613,
            "function": "match",
            "class": "Illuminate\\Routing\\RouteCollection",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 602,
            "function": "findRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Router.php",
            "line": 591,
            "function": "dispatchToRoute",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 176,
            "function": "dispatch",
            "class": "Illuminate\\Routing\\Router",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 30,
            "function": "Illuminate\\Foundation\\Http\\{closure}",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/fideloper\/proxy\/src\/TrustProxies.php",
            "line": 57,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Fideloper\\Proxy\\TrustProxies",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/TransformsRequest.php",
            "line": 30,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\TransformsRequest",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/ValidatePostSize.php",
            "line": 27,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\ValidatePostSize",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Middleware\/CheckForMaintenanceMode.php",
            "line": 46,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 149,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Middleware\\CheckForMaintenanceMode",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Routing\/Pipeline.php",
            "line": 53,
            "function": "Illuminate\\Pipeline\\{closure}",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Pipeline\/Pipeline.php",
            "line": 102,
            "function": "Illuminate\\Routing\\{closure}",
            "class": "Illuminate\\Routing\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 151,
            "function": "then",
            "class": "Illuminate\\Pipeline\\Pipeline",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Http\/Kernel.php",
            "line": 116,
            "function": "sendRequestThroughRouter",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 139,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Http\\Kernel",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/AbstractGenerator.php",
            "line": 125,
            "function": "callRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Generators\/LaravelGenerator.php",
            "line": 79,
            "function": "getRouteResponse",
            "class": "Mpociot\\ApiDoc\\Generators\\AbstractGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 264,
            "function": "processRoute",
            "class": "Mpociot\\ApiDoc\\Generators\\LaravelGenerator",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/mpociot\/laravel-apidoc-generator\/src\/Mpociot\/ApiDoc\/Commands\/GenerateDocumentation.php",
            "line": 85,
            "function": "processLaravelRoutes",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "function": "handle",
            "class": "Mpociot\\ApiDoc\\Commands\\GenerateDocumentation",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 29,
            "function": "call_user_func_array"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 87,
            "function": "Illuminate\\Container\\{closure}",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/BoundMethod.php",
            "line": 31,
            "function": "callBoundMethod",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Container\/Container.php",
            "line": 564,
            "function": "call",
            "class": "Illuminate\\Container\\BoundMethod",
            "type": "::"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 183,
            "function": "call",
            "class": "Illuminate\\Container\\Container",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Command\/Command.php",
            "line": 252,
            "function": "execute",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Command.php",
            "line": 170,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Command\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 865,
            "function": "run",
            "class": "Illuminate\\Console\\Command",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 241,
            "function": "doRunCommand",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/symfony\/console\/Application.php",
            "line": 143,
            "function": "doRun",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Console\/Application.php",
            "line": 88,
            "function": "run",
            "class": "Symfony\\Component\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/vendor\/laravel\/framework\/src\/Illuminate\/Foundation\/Console\/Kernel.php",
            "line": 121,
            "function": "run",
            "class": "Illuminate\\Console\\Application",
            "type": "->"
        },
        {
            "file": "\/Users\/ovac\/codes\/omnile\/booconnect\/artisan",
            "line": 37,
            "function": "handle",
            "class": "Illuminate\\Foundation\\Console\\Kernel",
            "type": "->"
        }
    ]
}
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
-H "Accept: application/json"
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
-H "Accept: application/json"
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

