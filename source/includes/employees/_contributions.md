## Add / Update a Plan for an Employee

```shell
curl -X "POST" "http://localhost:3210/plans/2/relationships/employees" \\
     -H 'x-api-key: localAPIKey' \\
     -H 'tio-auth-token: 123...' \\
     -H 'Content-Type: application/vnd.api+json' \\
     -d $'{
  "data": [
    { "type": "employees", "id": <EMPLOYEE_ID> }
  ]
}'
```

> Returns "204 No Content" on success

This endpoint attaches a contribution plan to a specific employee.

### HTTP Request

`POST https://crunchy-api.tio-vdk.io/employees/<PLAN_ID>/relationships/employees`

### URL Parameters

Parameter | Description
--------- | -----------
PLAN_ID | The PLAN_ID to attach to employee

### BODY Parameters

Parameter | Description
--------- | -----------
EMPLOYEE_ID | The EMPLOYEE_ID to receiving the contribution

## Remove a Plan from an Employee

```shell
curl -X "DELETE" "http://localhost:3210/plans/2/relationships/employees" \\
     -H 'x-api-key: localAPIKey' \\
     -H 'tio-auth-token: 123...' \\
     -H 'Content-Type: application/vnd.api+json' \\
     -d $'{
  "data": [
    { "type": "employees", "id": "3" }
  ]
}'
```

> Returns "204 No Content" on success

This endpoint removes a contribution plan from a specific employee.

### HTTP Request

`DELETE https://crunchy-api.tio-vdk.io/employees/<PLAN_ID>/relationships/employees`

### URL Parameters

Parameter | Description
--------- | -----------
PLAN_ID | The PLAN_ID to attach to employee

### BODY Parameters

Parameter | Description
--------- | -----------
EMPLOYEE_ID | The EMPLOYEE_ID to receiving the contribution

