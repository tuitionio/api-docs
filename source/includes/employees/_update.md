## Update a Specific Employee

```shell
curl -X PUT "https://crunchy-api.tio-vdk.io/employees/<ID>" \\
     -H 'x-api-key: meowmeowmeow' \\
     -H 'tio-auth-token: eyJhbGciOiJIUzUxMiJ9...' \\
     -d $'{
       "data": {
          id: "4064",
          "type": "employees",
          "attributes": {
            "first-name": "Anna Changed"
          }
       }
      }'
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "id": "4064",
    "type":"employees",
    "attributes": {
      "first-name": "Anna Changed",
      "last-name": "Riley",
      "email": "anna@test.com"
    }
  }
}
```

This endpoint updates a specific employee.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`PUT https://crunchy-api.tio-vdk.io/employees/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the employee to update