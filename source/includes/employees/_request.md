## Get a Specific Employee

```shell
curl "https://crunchy-api.tio-vdk.io/employees/<ID>" \\
     -H 'x-api-key: meowmeowmeow' \\
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

This endpoint retrieves a specific employee.

### HTTP Request

`GET https://crunchy-api.tio-vdk.io/employees/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the employee to retrieve