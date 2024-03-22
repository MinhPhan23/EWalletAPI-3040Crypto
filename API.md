# API Documentation for 3040 Crypto User API

## Introduction

With the 3040 Crypto User API, users can get their data and transaction histories in relation to the platform. Developers can use this API to retrieve details about users and their associated transactions.


## List of endpoints
### 1. `api/user/`
-  Retrieves information about all users registered on the platform.

### 2. `api/user/{user-id}/`
- Retrieves information about a specific user based on their User ID.

### 3. `GET api/user/{user-id}/transaction/`
- Retrieves transaction history for a specific user based on their User ID.


## Description of Resources

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

## Sample Requests and Responses

### 1. Get information of all user

#### Request

```bash
curl -X GET https://3040Crypto/api/user/
```

#### Response

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

### 2. Get information of a specific user

#### Request

```bash
curl -X GET https://3040Crypto/api/user/1
```

#### Response

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

### 3. Get all transaction from a specific user

#### Request

``` bash
curl -X GET https://3040Crypto/api/user/1/transaction
```

#### Response

``` json
200 OK
Content-Type: application/json

{
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

### Contributors
- [Dhairya Prajapati](https://github.com/dhairyahp15)
- [Huzaifa Mehboob](https://github.com/Huzzaifaa)
- [Minh Phan](https://github.com/MinhPhan23)
