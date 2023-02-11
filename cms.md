# ALL API'S

* [GET_CURRENT_BUILD_VERSION](#GET_CURRENT_BUILD_VERSION)

## GET_CURRENT_BUILD_VERSION

### Flow
* Required Fields: []

**URL** : `/dev/api/v1/getCurrentBuildVersion`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : None
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "action": "GET_CURRENT_BUILD_VERSION",
    "success": true,
    "message": "Fetched successfully.",
    "response": [
        {
            "_id": "63e7da1fe51b80bf09cfb3dd",
            "buildVersion": "16.13.0"
        }
    ]
}
```