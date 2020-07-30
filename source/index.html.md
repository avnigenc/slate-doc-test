---
title: masraff API v1 v1
language_tabs:
  - http: HTTP
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="masraff-api-v1">masraff API v1 v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Masraff API Version 1

Email: <a href="mailto:developer@masraff.co">Support</a> 

<h1 id="masraff-api-v1-expenses">Expenses</h1>

Expenses

## getAll

<a id="opIdgetAll"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/WeatherForecast \
  -H 'Accept: text/plain'

```

```http
GET /api/v1/WeatherForecast HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.get '/api/v1/WeatherForecast',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.get('/api/v1/WeatherForecast', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/WeatherForecast', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/WeatherForecast", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/WeatherForecast`

*Get Expenses Metadata For Company*

Requires admin privileges

> Example responses

> 201 Response

```
{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}
```

```json
{
  "date": "2019-08-24T14:15:22Z",
  "temperatureC": 0,
  "temperatureF": 0,
  "summary": "string"
}
```

<h3 id="getall-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|The product was created|[WeatherForecast](#schemaweatherforecast)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|The product data is invalid|[ProblemDetails](#schemaproblemdetails)|

<aside class="success">
This operation does not require authentication
</aside>

## getById

<a id="opIdgetById"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/WeatherForecast/getById \
  -H 'Accept: text/plain'

```

```http
GET /api/v1/WeatherForecast/getById HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast/getById',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.get '/api/v1/WeatherForecast/getById',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.get('/api/v1/WeatherForecast/getById', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/WeatherForecast/getById', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast/getById");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/WeatherForecast/getById", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/WeatherForecast/getById`

*Get Expenses Metadata For SubCompany*

Requires admin privileges

> Example responses

> 200 Response

```
[{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}]
```

```json
[
  {
    "date": "2019-08-24T14:15:22Z",
    "temperatureC": 0,
    "temperatureF": 0,
    "summary": "string"
  }
]
```

<h3 id="getbyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|

<h3 id="getbyid-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WeatherForecast](#schemaweatherforecast)]|false|none|none|
|» date|string(date-time)|false|none|none|
|» temperatureC|integer(int32)|false|none|none|
|» temperatureF|integer(int32)|false|read-only|none|
|» summary|string¦null|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="masraff-api-v1-expense-forms">Expense Forms</h1>

Expense Forms

## AddForecast

<a id="opIdAddForecast"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/WeatherForecast/AddForecast1 \
  -H 'Accept: text/plain'

```

```http
POST /api/v1/WeatherForecast/AddForecast1 HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast/AddForecast1',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.post '/api/v1/WeatherForecast/AddForecast1',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.post('/api/v1/WeatherForecast/AddForecast1', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/WeatherForecast/AddForecast1', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast/AddForecast1");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/WeatherForecast/AddForecast1", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/WeatherForecast/AddForecast1`

*Get Expense Form Metadata For Company*

Requires admin privileges

> Example responses

> 200 Response

```
[{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}]
```

```json
[
  {
    "date": "2019-08-24T14:15:22Z",
    "temperatureC": 0,
    "temperatureF": 0,
    "summary": "string"
  }
]
```

<h3 id="addforecast-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|

<h3 id="addforecast-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WeatherForecast](#schemaweatherforecast)]|false|none|none|
|» date|string(date-time)|false|none|none|
|» temperatureC|integer(int32)|false|none|none|
|» temperatureF|integer(int32)|false|read-only|none|
|» summary|string¦null|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="masraff-api-v1-forms">Forms</h1>

Forms

## AddForecast

<a id="opIdAddForecast"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/WeatherForecast/AddForecast2 \
  -H 'Accept: text/plain'

```

```http
POST /api/v1/WeatherForecast/AddForecast2 HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast/AddForecast2',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.post '/api/v1/WeatherForecast/AddForecast2',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.post('/api/v1/WeatherForecast/AddForecast2', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/WeatherForecast/AddForecast2', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast/AddForecast2");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/WeatherForecast/AddForecast2", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/WeatherForecast/AddForecast2`

*Create Custom Report*

Requires admin privileges

> Example responses

> 200 Response

```
[{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}]
```

```json
[
  {
    "date": "2019-08-24T14:15:22Z",
    "temperatureC": 0,
    "temperatureF": 0,
    "summary": "string"
  }
]
```

<h3 id="addforecast-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|

<h3 id="addforecast-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WeatherForecast](#schemaweatherforecast)]|false|none|none|
|» date|string(date-time)|false|none|none|
|» temperatureC|integer(int32)|false|none|none|
|» temperatureF|integer(int32)|false|read-only|none|
|» summary|string¦null|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="masraff-api-v1-company">Company</h1>

Company

## AddForecast

<a id="opIdAddForecast"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/WeatherForecast/AddForecast3 \
  -H 'Accept: text/plain'

```

```http
POST /api/v1/WeatherForecast/AddForecast3 HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast/AddForecast3',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.post '/api/v1/WeatherForecast/AddForecast3',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.post('/api/v1/WeatherForecast/AddForecast3', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/WeatherForecast/AddForecast3', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast/AddForecast3");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/WeatherForecast/AddForecast3", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/WeatherForecast/AddForecast3`

*Create Company*

Requires admin privileges

> Example responses

> 200 Response

```
[{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}]
```

```json
[
  {
    "date": "2019-08-24T14:15:22Z",
    "temperatureC": 0,
    "temperatureF": 0,
    "summary": "string"
  }
]
```

<h3 id="addforecast-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|

<h3 id="addforecast-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WeatherForecast](#schemaweatherforecast)]|false|none|none|
|» date|string(date-time)|false|none|none|
|» temperatureC|integer(int32)|false|none|none|
|» temperatureF|integer(int32)|false|read-only|none|
|» summary|string¦null|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="masraff-api-v1-tag2">tag2</h1>

## AddForecast

<a id="opIdAddForecast"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/WeatherForecast/AddForecast \
  -H 'Accept: text/plain'

```

```http
POST /api/v1/WeatherForecast/AddForecast HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast/AddForecast',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.post '/api/v1/WeatherForecast/AddForecast',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.post('/api/v1/WeatherForecast/AddForecast', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/WeatherForecast/AddForecast', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast/AddForecast");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/WeatherForecast/AddForecast", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/WeatherForecast/AddForecast`

*Add new forecast*

Requires admin privileges

> Example responses

> 200 Response

```
[{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}]
```

```json
[
  {
    "date": "2019-08-24T14:15:22Z",
    "temperatureC": 0,
    "temperatureF": 0,
    "summary": "string"
  }
]
```

<h3 id="addforecast-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|

<h3 id="addforecast-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WeatherForecast](#schemaweatherforecast)]|false|none|none|
|» date|string(date-time)|false|none|none|
|» temperatureC|integer(int32)|false|none|none|
|» temperatureF|integer(int32)|false|read-only|none|
|» summary|string¦null|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="masraff-api-v1-tags">Tags</h1>

## AddForecast

<a id="opIdAddForecast"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/WeatherForecast/AddForecast4 \
  -H 'Accept: text/plain'

```

```http
POST /api/v1/WeatherForecast/AddForecast4 HTTP/1.1

Accept: text/plain

```

```javascript

const headers = {
  'Accept':'text/plain'
};

fetch('/api/v1/WeatherForecast/AddForecast4',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/plain'
}

result = RestClient.post '/api/v1/WeatherForecast/AddForecast4',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'text/plain'
}

r = requests.post('/api/v1/WeatherForecast/AddForecast4', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/WeatherForecast/AddForecast4', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/WeatherForecast/AddForecast4");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/WeatherForecast/AddForecast4", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/WeatherForecast/AddForecast4`

*Get Tags Metadata For Company*

Requires admin privileges

> Example responses

> 200 Response

```
[{"date":"2019-08-24T14:15:22Z","temperatureC":0,"temperatureF":0,"summary":"string"}]
```

```json
[
  {
    "date": "2019-08-24T14:15:22Z",
    "temperatureC": 0,
    "temperatureF": 0,
    "summary": "string"
  }
]
```

<h3 id="addforecast-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|

<h3 id="addforecast-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WeatherForecast](#schemaweatherforecast)]|false|none|none|
|» date|string(date-time)|false|none|none|
|» temperatureC|integer(int32)|false|none|none|
|» temperatureF|integer(int32)|false|read-only|none|
|» summary|string¦null|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_WeatherForecast">WeatherForecast</h2>
<!-- backwards compatibility -->
<a id="schemaweatherforecast"></a>
<a id="schema_WeatherForecast"></a>
<a id="tocSweatherforecast"></a>
<a id="tocsweatherforecast"></a>

```json
{
  "date": "2019-08-24T14:15:22Z",
  "temperatureC": 0,
  "temperatureF": 0,
  "summary": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|date|string(date-time)|false|none|none|
|temperatureC|integer(int32)|false|none|none|
|temperatureF|integer(int32)|false|read-only|none|
|summary|string¦null|false|none|none|

<h2 id="tocS_ProblemDetails">ProblemDetails</h2>
<!-- backwards compatibility -->
<a id="schemaproblemdetails"></a>
<a id="schema_ProblemDetails"></a>
<a id="tocSproblemdetails"></a>
<a id="tocsproblemdetails"></a>

```json
{
  "type": "string",
  "title": "string",
  "status": 0,
  "detail": "string",
  "instance": "string",
  "property1": {},
  "property2": {}
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|**additionalProperties**|object|false|none|none|
|type|string¦null|false|none|none|
|title|string¦null|false|none|none|
|status|integer(int32)¦null|false|none|none|
|detail|string¦null|false|none|none|
|instance|string¦null|false|none|none|

