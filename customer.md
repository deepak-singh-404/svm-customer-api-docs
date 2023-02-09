# ALL API'S

* [GET_CUSTOMER_PROFILE](#GET_CUSTOMER_PROFILE)
* [GET_WALLET_TRANSACTIONS](#GET_WALLET_TRANSACTIONS)
* [GET_CUSTOMER_WALLET](#GET_CUSTOMER_WALLET)


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
        },
        {
            "_id": "63b47e33302fe4b207288a05",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-03T19:12:51.844Z"
        },
        {
            "_id": "63b47e39302fe4b207288a13",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-03T19:12:57.621Z"
        },
        {
            "_id": "63b47e3a302fe4b207288a21",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-03T19:12:58.809Z"
        },
        {
            "_id": "63b5b050abb56ca4d51a3923",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-04T16:58:56.857Z"
        },
        {
            "_id": "63b5b052abb56ca4d51a3931",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-04T16:58:58.474Z"
        },
        {
            "_id": "63b5b053abb56ca4d51a393f",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-04T16:58:59.744Z"
        },
        {
            "_id": "63b5b055abb56ca4d51a394d",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-04T16:59:01.097Z"
        },
        {
            "_id": "63b5b10be12d259a64ae7557",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-02",
            "createdAt": "2023-01-04T17:02:03.088Z"
        },
        {
            "_id": "63b5b1d5096e8e0df6742023",
            "customer": "636e30e1ff17b27d5e9d7ef5",
            "transactionType": "credit",
            "transactionAmount": 100,
            "transactionDescription": "referAndEarn",
            "validUpto": "2023-02-03",
            "createdAt": "2023-01-04T17:05:25.862Z"
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