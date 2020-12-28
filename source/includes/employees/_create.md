## Create Employee
```shell

curl -X "POST" "http://localhost:3210/employees" \\
     -H 'x-api-key: localAPIKey' \\
     -H 'tio-auth-token: eyJhbGciOiJIUzUxMiJ9..' \\
     -H 'Content-Type: application/vnd.api+json' \\
     -d $'{
        "data": {
          "type": "employees",
          "attributes": {
            "first-name": "Cory",
            "last-name": "Loken",
            "payroll-id": "32191"
          },
          "relationships": {
            "company": {
              "data": {
                "type": "companies",
                "id": "<COMPANY_ID>"
              }
            }
          }
        }
      }'
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "id":"3",
    "type":"employees",
    "attributes": {
      "first-name": "Cory",
      "last-name": "Loken",
      "email": null,
      "payroll-id": "32191"
    }
  }
}
```

This endpoint creates a specific employee.

### HTTP Request

`POST https://crunchy-api.tio-vdk.io/employees`

### BODY Parameters

Parameter | Description
--------- | -----------
COMPANY_ID | The COMPANY_ID of the employee to create
