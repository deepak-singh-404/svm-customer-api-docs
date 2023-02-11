# ALL API'S

* [GET_CURRENT_BUILD_VERSION](#GET_CURRENT_BUILD_VERSION)
* [GET_UTILITY_CONTENT](#GET_UTILITY_CONTENT)

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

## GET_UTILITY_CONTENT

### Flow
* Required Params: [type]

**URL** : `/dev/api/v1/getUtilityContent`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : None
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "action": "GET_UTILITY_CONTENT",
    "success": true,
    "message": "Fetched successfully.",
    "count": 1,
    "response": [
        {
            "_id": "63e7e269d306823f2081bfb0",
            "contentType": "HOMESCREEN_BANNER",
            "picture": "https://prod-utility-content.s3.ap-south-1.amazonaws.com/IMAGES/HOMESCREEN_BANNER/Screenshot%20from%202023-01-30%2013-11-25.png",
            "title": "1",
            "index": 1,
            "redirectionUrl": "",
            "createdAt": "2023-02-11T18:46:01.881Z",
            "updatedAt": "2023-02-11T18:46:01.881Z",
            "__v": 0
        }
    ]
}
```