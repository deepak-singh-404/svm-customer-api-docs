# ALL API'S

* [GET_CUSTOMER_PROFILE](#GET_CUSTOMER_PROFILE)
* [GET_WALLET_TRANSACTIONS](#GET_WALLET_TRANSACTIONS)
* [GET_CUSTOMER_WALLET](#GET_CUSTOMER_WALLET)
* [ADD_ADDRESS](#ADD_ADDRESS)
* [GET_ADDRESS_OF_CUSTOMER](#GET_ADDRESS_OF_CUSTOMER)


## GET_CUSTOMER_PROFILE

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/getCustomerProfile`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "success": true,
    "statusCode": 200,
    "action": "GET_CUSTOMER_PROFILE-0c60c53e-a7b4-48fe-9cfe-b216126edc8f",
    "message": "Ok.",
    "response": {
        "lastServiceAddress": {
            "name": "Deepak Singh",
            "zipcode": 201305,
            "phoneNumber": "+919415332242",
            "city": "Noida",
            "state": "Uttar Pradesh",
            "coordinates": []
        },
        "_id": "636e30e1ff17b27d5e9d7ef5",
        "walletAmount": 1200,
        "cityName": "Jaipur",
        "email": "Web.dev.deepaksingh@gmail.com",
        "name": "Deepak Singh"
    }
}
```

## GET_WALLET_TRANSACTIONS

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/wallet/transactions`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "success": true,
    "statusCode": 200,
    "action": "WALLET_TRANSACTIONS-00665264-59a8-47b3-8ee9-0b9584634211",
    "message": "Fetched successfully.",
    "count": 11,
    "response": [
        {
            "_id": "637a506fd23b8db4ba501ef7",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 200,
            "transactionDescription": "200 amount has been credited.",
            "validUpto": "2022-12-21",
            "createdAt": "2022-11-20T16:06:07.155Z"
        },
        {
            "_id": "63b47e12302fe4b2072889f7",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-03T19:12:18.506Z"
        }
    ]
}
```

## GET_CUSTOMER_WALLET

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/getCustomerWallet`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "success": true,
    "statusCode": 200,
    "action": "GET_CUSTOMER_WALLET-90d31971-4a24-4005-a8b3-26be44d25fe9",
    "message": "Fetched successfully.",
    "response": {
        "_id": "63e3deabeae095c783560fde",
        "customer": "6324a8acd91690055b2b768c",
        "referralAmount": 100,
        "refundAmount": 0,
        "cashback": 0,
        "totalWalletAmount": 100,
        "createdAt": "2023-02-08T17:40:59.382Z",
        "updatedAt": "2023-02-08T17:40:59.382Z",
        "__v": 0
    }
}
```


## ADD_ADDRESS

### Flow
* Required Fields: ["customerId", "address", "save"]

**URL** : `/dev/api/v1/addAddress`
**Method** : `POST`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Request Body 
```json
{
    "customerId": "636e30e1ff17b27d5e9d7ef5",
    "address": {
        "name": "Deepak Singh",
        "houseNo": "B 80 2",
        "phoneNumber": "+919415332242",
        "coordinates": [],
        "landmark": "Near Sanjay Properties 2",
        "zipcode": "201301"
    },
    "save": true
}
```
## Success Response 
**Code** : `200`
**Response**
```json
{
    "success": true,
    "message": "Address saved successfully",
    "response": {
        "_id": "636e30e1ff17b27d5e9d7ef5",
        "savedAddress": [
            {
                "name": "Deepak Singh",
                "zipcode": 201301,
                "phoneNumber": "+919415332242",
                "houseNo": "B 80 2",
                "landmark": "Near Sanjay Properties 2",
                "coordinates": [],
                "_id": "63edcb95271f41ef7b08ff1d"
            },
            {
                "name": "Nishant",
                "zipcode": 94043,
                "phoneNumber": "8521824578",
                "houseNo": "VR PG",
                "landmark": "Room -403",
                "coordinates": [
                    37.4217937,
                    -122.083922
                ],
                "_id": "63e67840afcffb85bc772925"
            }
        ]
    },
    "action": "add_address"
}
```

## GET_ADDRESS_OF_CUSTOMER

### Flow
* Required Params: ["customerId"]

**URL** : `/dev/api/v1/getCustomerAddress?customerId=636e30e1ff17b27d5e9d7ef5`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "action": "GET_ADDRESS_OF_CUSTOMER",
    "success": true,
    "message": "Fetched successfully.",
    "response": {
        "defaultAddress": {
            "city": "Noida",
            "coordinates": [],
            "houseNo": "B 80 2",
            "landmark": "Near Sanjay Properties 2",
            "name": "Deepak Singh",
            "phoneNumber": "+919415332242",
            "state": "Uttar Pradesh",
            "zipcode": 201301
        },
        "lastServiceAddress": {
            "name": "Deepak Singh",
            "zipcode": 201305,
            "phoneNumber": "+919415332242",
            "city": "Noida",
            "state": "Uttar Pradesh",
            "coordinates": []
        },
        "_id": "636e30e1ff17b27d5e9d7ef5",
        "savedAddress": [
            {
                "name": "Deepak Singh",
                "zipcode": 201301,
                "phoneNumber": "+919415332242",
                "houseNo": "B 80 2",
                "landmark": "Near Sanjay Properties 2",
                "coordinates": [],
                "_id": "63edcb95271f41ef7b08ff1d"
            },
            {
                "name": "Deepak Singh",
                "zipcode": 201305,
                "phoneNumber": "+919415332242",
                "houseNo": "B 80",
                "landmark": "Near Sanjay Properties",
                "coordinates": [],
                "_id": "63edcabc271f41ef7b08ff06"
            },
            {
                "name": "Nishant",
                "zipcode": 94043,
                "phoneNumber": "8521824578",
                "houseNo": "VR PG",
                "landmark": "Room -404",
                "coordinates": [
                    37.4217937,
                    -122.083922
                ],
                "_id": "63e6787eafcffb85bc77292d"
            },
            {
                "name": "Nishant",
                "zipcode": 94043,
                "phoneNumber": "8521824578",
                "houseNo": "VR PG",
                "landmark": "Room -403",
                "coordinates": [
                    37.4217937,
                    -122.083922
                ],
                "_id": "63e67840afcffb85bc772925"
            }
        ]
    }
}
```