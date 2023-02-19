# ALL API'S

* [CANCEL_BOOKING](#CANCEL_BOOKING)
* [RESCHEDULE_SERVICE](#RESCHEDULE_SERVICE)


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


## RESCHEDULE_SERVICE

### Flow
* Required Fields: ["customerId", "timeSlot", "serviceDate", "bookingId"]
* Optional Fields: ["reason"]

**URL** : `/dev/api/v1/cancelBooking`
**Method** : `POST`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Request Body 
```json
{
    "customerId": "61f8f3f93dcaf8bebde5385b",
    "timeSlot": "10:30 AM",
    "serviceDate": "2023-02-20",
    "bookingId": "63f2275f75b889c41aa8f94b"
}
```
## Success Response 
**Code** : `200`
**Response**
```json
{
    "success": true,
    "message": "Booking Rescheduled Successfully",
    "response": {
        "customer": {
            "name": "Nishant",
            "email": "",
            "phoneNumber": "+917254844368"
        },
        "extraCharge": {
            "amount": 39,
            "_id": "61f78c565575e8e5dfc0d438",
            "name": "Hygenic Fee",
            "createdAt": "2023-02-19T13:42:55.914Z"
        },
        "bookingJourney": {
            "isStarted": false,
            "isStopped": false,
            "isCustomerPaid": false,
            "amountPaidByCustomer": 0
        },
        "_id": "63f2275f75b889c41aa8f94b",
        "bookingId": 1452,
        "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
        "services": [
            {
                "serviceCategory": "61f7a207e6bfed403ad9b79d",
                "serviceName": "Beauty Valley",
                "serviceId": "61f807aa512294e7ac80d1ba",
                "actualPrice": 1198,
                "discountedPrice": 780,
                "quantity": 1,
                "_id": "63f2224175b889c41aa8f75e",
                "createdAt": "2023-02-19T13:21:05.890Z"
            }
        ],
        "customerId": "61f8f3f93dcaf8bebde5385b",
        "address": {
            "name": "Nishant",
            "address": "1600 Amphitheatre Pkwy, Mountain View, CA 94043, USA",
            "phoneNumber": "+917254844368",
            "zipcode": 123457,
            "coordinates": [
                37.4220936,
                -122.083922
            ],
            "landmark": "Beir Library",
            "houseNo": "N-202"
        },
        "serviceDate": "2023-02-20",
        "timeSlot": "10:30 AM",
        "modeOfPayment": "COD",
        "isPaid": false,
        "isServiceProviderAssigned": false,
        "isJobDone": false,
        "isRequestedToCancelService": false,
        "rating": 0,
        "isCancelled": false,
        "isCustomerCancelledService": false,
        "isAdminCancelledService": false,
        "finalPrice": 819,
        "cartAmount": 780,
        "isAdminApprovedCancellationRequest": false,
        "requestedServiceProviders": [
            "63c82cedc14c1d5b21f04077"
        ],
        "systemOrManual": 0,
        "isFeedbackGivenByCustomer": false,
        "formattedTimestamp": "2023-02-19 13:44:33",
        "timeOfBooking": "2023-02-19T13:42:55.954Z",
        "createdAt": "2023-02-19T13:42:55.954Z",
        "approvedAt": "2023-02-19T13:42:55.954Z",
        "__v": 0
    },
    "action": "reschedule service"
}
```