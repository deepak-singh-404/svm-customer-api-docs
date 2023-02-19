# ALL API'S

* [GET_NOTIFICATION](#GET_NOTIFICATION)
* [DISMISS_NOTIFICATION](#DISMISS_NOTIFICATION)


## GET_NOTIFICATION

### Flow
* Required Params: [customerId]

**URL** : `dev/api/v1/getNotifications?customerId=636e30e1ff17b27d5e9d7ef5`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "action": "GET_NOTIFICATIONS",
    "response": {
        "BOOKING_PROCESSING": {
            "show": true,
            "notificationId": "63dd2d195770b3f95b67cb0f",
            "metaData": {
                "dismissCount": 0,
                "metaData": {
                    "bookingId": 1437
                }
            }
        },
        "PARTNER_ASSIGNED": {
            "show": false,
            "metaData": {}
        },
        "BOOKING_COMPLETED": {
            "show": false,
            "metaData": {}
        }
    }
}
```

## DISMISS_NOTIFICATION

### Flow
* Required Params: [notificationId, type]

**URL** : `dev/api/v1/dismissNotification?notid=63dd2d195770b3f95b67cb0f&type=BOOKING_PROCESSING`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "action": "DISMISS_NOTIFICATION",
    "success": true,
    "message": "Dismissed successfully.",
    "response": null
}
```