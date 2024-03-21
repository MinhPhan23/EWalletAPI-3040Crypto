# Introduction

# List of endpoint
- GET api/user/
- GET api/user/{user-id}/
- GET api/user/{user-id}/transaction/

# Resources

``` json
{
    "user-id" : 1,
    "name" : "Minh",
    "email" : "sth@umanitoba.ca",
    "dob" : "MM/DD/YYYY",
    "transaction" : [
        {
            "trans-id" : 1,
            "currency" : "BTC",
            "ammount" : 10,
            "type" : "deposit"
        },
        {
            "trans-id" : 2,
            "currency" : "ETH",
            "ammount" : 10,
            "type" : "withdrawal"
        }
    ]
}
```

# Sample

## Get information of all user

### Request

```bash
curl https://3040Crypto/api/user/
```

### Response

``` json
200 OK
Content-Type: application/json

{
    "user-info" : [
        {
            "user-id" : 1,
            "name" : "Minh",
            "email" : "sth@umanitoba.ca",
            "dob" : "20/01/1960",
        },
        {
            "user-id" : 2,
            "name" : "Xia",
            "email" : "sth@umanitoba.ca",
            "dob" : "23/12/2000",
        },
    ]
}
```

## Get information of a specific user

### Request

```bash
curl https://3040Crypto/api/user/1
```

### Response

``` json
200 OK
Content-Type: application/json

{
    "user-id" : 1,
    "name" : "Minh",
    "email" : "sth@umanitoba.ca",
    "dob" : "20/01/1960",
}
```

## Get all transaction from a specific user

``` bash
curl https://3040Crypto/api/user/1/transaction
```

### Response

``` json
200 OK
Content-Type: application/json

{
    "user-id" : 1,
    "name" : "Minh",
    "email" : "sth@umanitoba.ca",
    "dob" : "20/01/1960",
    "transaction" : [
        {
            "trans-id" : 1,
            "currency" : "BTC",
            "ammount" : 10,
            "type" : "deposit"
        },
        {
            "trans-id" : 2,
            "currency" : "ETH",
            "ammount" : 10,
            "type" : "withdrawal"
        }
    ]
}
```