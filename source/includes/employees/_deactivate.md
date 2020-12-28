## Deactivate a Specific Employee

```shell
curl -X "DELETE" "http://localhost:3210/employees/<ID>" \\
     -H 'x-api-key: meowmeowmeow' \\
     -H 'tio-auth-token: 'purrpurrpurr' \\
     -H 'Content-Type: application/json; charset=utf-8'
```

This endpoint deactivates a specific employee.

### HTTP Request

`DELETE https://crunchy-api.tio-vdk.io/employees/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the employee to deactivate