# ALL API'S

* [CANCEL_BOOKING](#CANCEL_BOOKING)


## CANCEL_BOOKING

### Flow
* Required Fields: ["customerId","bookingId"]
* Optional Fields: ["reason"]

**URL** : `/dev/api/v1/cancelBooking`
**Method** : `POST`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Request Body 
```json
{
    "customerId":"636e30e1ff17b27d5e9d7ef5",
    "bookingId":"63aeec28245b98838f7cc2d1",
    "reason":"Api testing."
}
```
## Success Response 
**Code** : `200`
**Response**
```json
{
    "success": true,
    "message": "Cancelled successfully.",
    "response": {
        "customer": {
            "name": "Deepak Singh",
            "email": "Web.dev.deepaksingh@gmail.com",
            "phoneNumber": "+919415332242"
        },
        "_id": "63aeec28245b98838f7cc2d1",
        "customerId": "636e30e1ff17b27d5e9d7ef5",
        "isServiceProviderAssigned": false,
        "isJobDone": false,
        "isRequestedToCancelService": false,
        "isCancelled": true,
        "isCustomerCancelledService": true,
        "cancelledAt": "2023-01-19T14:05:09.393Z",
        "customerCancelledServiceAt": "2023-01-19T14:05:09.393Z",
        "customerCancellationReason": "Api testing."
    },
    "action": "CANCEL_BOOKING-a252afd7-2cff-4468-8df6-353ad48547e8"
}
```

