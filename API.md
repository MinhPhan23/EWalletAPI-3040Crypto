# Introduction

# List of endpoint
- GET api/user/
- GET api/user/{user-id}/
- GET api/user/{user-id}/transaction/
- GET api/user/{user-id}/transaction/{trans-id}

# Resources

``` python
{
    "user" : {
        "user-id" : 12,
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
}
```

# Sample

## Requests

## Response