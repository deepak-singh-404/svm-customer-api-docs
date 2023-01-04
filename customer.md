# ALL API'S

* [GET_CUSTOMER_PROFILE](#GET_CUSTOMER_PROFILE)

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