# ALL API'S

* [GENERATE_REFERRAL_CODE](#GENERATE_REFERRAL_CODE)

## GENERATE_REFERRAL_CODE

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/voucher/generateReferralCode`
**Method** : `POST`
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
