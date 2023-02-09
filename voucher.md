# ALL API'S

* [GENERATE_REFERRAL_CODE](#GENERATE_REFERRAL_CODE)
* [REDEEM_REFERRAL_CODE](#REDEEM_REFERRAL_CODE)
* [GET_CUSTOMER_PROFILE](#GET_CUSTOMER_PROFILE)
* [GET_REFERRAL_CODE](#GET_REFERRAL_CODE)
* [APPLY_REFERRAL_CODE](#APPLY_REFERRAL_CODE)

## GENERATE_REFERRAL_CODE

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/voucher/generateReferralCode`
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
    "action": "GENERATE_REFERRAL_CODE-b1d3e75e-f6d4-4419-9035-99f7fcae3bdc",
    "message": "Coupon generated successfully.",
    "response": {
        "_id": "63b45958fa35619baa19b828",
        "referralCode": "DEE114"
    }
}
```

## REDEEM_REFERRAL_CODE

### Flow
* Required Params: [referralCode]

**URL** : `/dev/api/v1/voucher/redeemReferralCode?referralCode=DEE116`
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
    "action": "REDEEM_REFERRAL_CODE-d90a7069-7a9e-4a71-8120-1df33715fb7f",
    "message": "Redeemed successfully",
    "response": {
        "_id": "63b5b1b9096e8e0df6742015",
        "referedBy": "636e30e1ff17b27d5e9d7ef5",
        "config": "63b457fb9691992f1ff6ba65",
        "referralCode": "DEE118",
        "referredByAmount": 100,
        "referralAmount": 100,
        "validUpto": "2023-02-03",
        "isUsed": true,
        "createdAt": "2023-01-04T17:04:57.693Z",
        "updatedAt": "2023-01-04T17:04:57.693Z",
        "__v": 0,
        "referral": "6324a8acd91690055b2b768c"
    }
}
```

## GET_REFERRAL_CODE

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/getReferralCode`
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
    "action": "GET_REFERRAL_CODE-4a907c53-3ed6-425b-b51c-d25d0ea70851",
    "message": "Fetched successfully.",
    "response": {
        "_id": "636e30e1ff17b27d5e9d7ef5",
        "phoneNumber": "+919415332242",
        "name": "Deepak Singh",
        "welcomeReferralCode": "DEE4228"
    }
}
```

## APPLY_REFERRAL_CODE

### Flow
* Required Params: [code]

**URL** : `/dev/api/v1/applyReferralCode?code=DEE4228`
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
    "action": "APPLY_REFERRAL_CODE-d90a7069-7a9e-4a71-8120-1df33715fb7f",
    "message": "Redeemed successfully",
    "response": {}
}
```