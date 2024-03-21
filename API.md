# Introduction

# List of endpoint
- GET api/user/
- GET api/user/{user-id}/
- GET api/user/{user-id}/transaction/

# Resources

``` json
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

## Get information of all user

### Request

```bash
curl https://3040Crypto/api/user/
```

### Response

## Get information of a specific user

### Request

```bash
curl https://3040Crypto/api/user/1
```

### Response

## Get all transaction from a specific user

``` bash
curl https://3040Crypto/api/user/1/transaction
```

### Response