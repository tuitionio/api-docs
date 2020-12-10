# Employees

## Get Employees

```shell
## Request Employees
curl "https://crunchy-api.tio-vdk.io/employees?page%5Blimit%5D=2" \
     -H 'x-api-key: meowmeowmeow' \
     -H 'tio-auth-token: eyJhbGciOiJIUzUxMiJ9...'
```

> The above command returns JSON structured like this:

```json
{
  "data":
    [{
      "id":"4064",
      "type":"employees",
      "attributes": {
        "first-name": "Anna",
        "last-name":"Riley",
        "email": "anna@test.com"
      }
    }, {
      "id":"4065",
      "type":"employees",
      "attributes": {
        "first-name":"Loren",
        "last-name":"Jefferson",
        "email": "loren@test.com"
      }
    }]
  },
  "meta": {
    "page": {
      "total": 140
    },
    "requester":10800,
    "copyright":"©2020"
  }
}
```

`GET https://crunchy-api.tio-vdk.io/employees?page%5Blimit%5D=2`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page[limit] | 500 | If set to true, the result will also include cats.
page[offset] | 0 | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — additional information is included in the response. See relations and parameters for more info.
</aside>

## Get a Specific Employee

```shell
curl "https://crunchy-api.tio-vdk.io/employees/<ID>" \
     -H 'x-api-key: meowmeowmeow' \
     -H 'tio-auth-token: eyJhbGciOiJIUzUxMiJ9...'
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "id": "4064",
    "type":"employees",
    "attributes": {
      "first-name": "Anna",
      "last-name": "Riley",
      "email": "anna@test.com"
    }
  }
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET https://crunchy-api.tio-vdk.io/employees/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the employee to retrieve

## Deactivate a Specific Employee

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deactivates a specific employee.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
