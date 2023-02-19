# ALL API'S

* [CANCEL_BOOKING](#CANCEL_BOOKING)
* [RESCHEDULE_SERVICE](#RESCHEDULE_SERVICE)
* [GET_ALL_BOOKINGS](#GET_ALL_BOOKINGS)


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

**URL** : `/dev/api/v1/rescheduleService`
**Method** : `PUT`
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

## GET_ALL_BOOKINGS

### Flow
* Required Params: ["customerId","type"]

**URL** : `/dev/api/v1/getAllBookings?customerId=636e30e1ff17b27d5e9d7ef5&type=PAST`
**Method** : `GET`
**Header** : `application/json`
**Auth required** : Yes
**Permissions required** : None

## Success Response 
**Code** : `200`
**Response**
```json
{
    "action": "GET_ALL_BOOKINGS",
    "message": "Fetched successfully.",
    "success": true,
    "count": 7,
    "response": [
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "type": "hygenic",
                "amount": 39
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "638f638436eae9f592952187",
            "bookingId": 1400,
            "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
            "services": [
                {
                    "serviceCategory": "61f7a207e6bfed403ad9b79d",
                    "serviceName": "Beauty Valley",
                    "serviceId": "61f807aa512294e7ac80d1ba",
                    "actualPrice": 1198,
                    "discountedPrice": 780,
                    "quantity": 2,
                    "_id": "638f632336eae9f59295216a",
                    "createdAt": "2022-12-06T15:43:31.334Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak singh",
                "phoneNumber": "9415332242",
                "zipcode": 113306,
                "city": "Gorakhpur",
                "state": "Uttar Pradesh",
                "coordinates": [
                    28.5162968,
                    77.2037341
                ],
                "landmark": "Landmark",
                "houseNo": "A401"
            },
            "serviceDate": "2022-12-07",
            "timeSlot": "01:30 PM  -  02:00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": true,
            "isCustomerCancelledService": false,
            "isAdminCancelledService": true,
            "finalPrice": 1599,
            "cartAmount": 1560,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "638f62e92de8804ce42499f7"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": true,
            "formattedTimestamp": "2022-12-06 12:37:13",
            "timeOfBooking": "2022-12-06T15:45:08.005Z",
            "createdAt": "2022-12-06T15:45:08.005Z",
            "approvedAt": "2022-12-06T15:45:08.005Z",
            "__v": 0,
            "adminCancellationReason": "Partner not available",
            "adminCancelledServiceAt": "2022-12-06T16:27:48.734Z",
            "cancelledAt": "2022-12-06T16:27:48.734Z"
        },
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "amount": 39,
                "_id": "61f78c565575e8e5dfc0d438",
                "name": "Hygenic Fee",
                "createdAt": "2022-12-29T19:33:02.004Z"
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "63adeb6edb7e5e4a6142c157",
            "bookingId": 1416,
            "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
            "services": [
                {
                    "serviceCategory": "61f7a207e6bfed403ad9b79d",
                    "serviceName": "V-Day",
                    "serviceId": "6311c0ebe4cf75b15829f1a9",
                    "actualPrice": 800,
                    "discountedPrice": 520,
                    "quantity": 1,
                    "_id": "63add6a8ac90faf21a8c4adb",
                    "createdAt": "2022-12-29T18:04:24.381Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak Singh",
                "zipcode": 201305,
                "phoneNumber": "+919415332242",
                "city": "Noida",
                "state": "Uttar Pradesh"
            },
            "serviceDate": "2023-01-01",
            "timeSlot": "01: 30 PM  -  02: 00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": true,
            "isCustomerCancelledService": true,
            "isAdminCancelledService": false,
            "finalPrice": 559,
            "cartAmount": 520,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "638c78a59e88e1358851ace6",
                "63adc234c182c881af2a8b44"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": false,
            "formattedTimestamp": "2022-12-30 01:02:58",
            "timeOfBooking": "2022-12-29T19:33:02.128Z",
            "createdAt": "2022-12-29T19:33:02.128Z",
            "approvedAt": "2022-12-29T19:33:02.128Z",
            "__v": 0,
            "cancelledAt": "2023-01-04T12:44:32.365Z",
            "customerCancelledServiceAt": "2023-01-04T12:44:32.365Z"
        },
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "amount": 39,
                "_id": "61f78c565575e8e5dfc0d438",
                "name": "Hygenic Fee",
                "createdAt": "2022-12-30T13:48:24.724Z"
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "63aeec28245b98838f7cc2d1",
            "bookingId": 1417,
            "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
            "services": [
                {
                    "serviceCategory": "61f7a207e6bfed403ad9b79d",
                    "serviceName": "V-Day",
                    "serviceId": "6311c0ebe4cf75b15829f1a9",
                    "actualPrice": 800,
                    "discountedPrice": 520,
                    "quantity": 1,
                    "_id": "63aeec28245b98838f7cc2c0",
                    "createdAt": "2022-12-30T13:48:24.619Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak Singh",
                "zipcode": 201305,
                "phoneNumber": "+919415332242",
                "city": "Noida",
                "state": "Uttar Pradesh"
            },
            "serviceDate": "2023-01-01",
            "timeSlot": "01: 30 PM  -  02: 00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": true,
            "isCustomerCancelledService": true,
            "isAdminCancelledService": false,
            "finalPrice": 559,
            "cartAmount": 520,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "638c78a59e88e1358851ace6",
                "63adc234c182c881af2a8b44"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": true,
            "formattedTimestamp": "2022-12-30 13:46:34",
            "timeOfBooking": "2022-12-30T13:48:24.742Z",
            "createdAt": "2022-12-30T13:48:24.742Z",
            "approvedAt": "2022-12-30T13:48:24.742Z",
            "__v": 0,
            "cancelledAt": "2023-01-19T14:05:09.393Z",
            "customerCancelledServiceAt": "2023-01-19T14:05:09.393Z",
            "customerCancellationReason": "Api testing."
        },
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "amount": 39,
                "_id": "61f78c565575e8e5dfc0d438",
                "name": "Hygenic Fee",
                "createdAt": "2023-01-26T17:08:36.045Z"
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "63d2b3943c69786a975553be",
            "bookingId": 1432,
            "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
            "services": [
                {
                    "serviceCategory": "61f7a207e6bfed403ad9b79d",
                    "serviceName": "V-Day",
                    "serviceId": "6311c0ebe4cf75b15829f1a9",
                    "actualPrice": 800,
                    "discountedPrice": 800,
                    "quantity": 1,
                    "_id": "63d2b3933c69786a975553ad",
                    "createdAt": "2023-01-26T17:08:35.929Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak Singh",
                "zipcode": 201305,
                "phoneNumber": "+919415332242",
                "city": "Noida",
                "state": "Uttar Pradesh"
            },
            "serviceDate": "2023-01-01",
            "timeSlot": "01: 30 PM  -  02: 00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": true,
            "isCustomerCancelledService": false,
            "isAdminCancelledService": true,
            "finalPrice": 839,
            "cartAmount": 800,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "63adc234c182c881af2a8b44",
                "63c82cedc14c1d5b21f04077"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": false,
            "formattedTimestamp": "2023-01-26 22:37:51",
            "timeOfBooking": "2023-01-26T17:08:36.064Z",
            "createdAt": "2023-01-26T17:08:36.064Z",
            "approvedAt": "2023-01-26T17:08:36.064Z",
            "__v": 0,
            "adminCancellationReason": "Test",
            "adminCancelledServiceAt": "2023-02-03T20:13:50.174Z",
            "cancelledAt": "2023-02-03T20:13:50.174Z"
        },
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "amount": 39,
                "_id": "61f78c565575e8e5dfc0d438",
                "name": "Hygenic Fee",
                "createdAt": "2023-02-02T17:24:41.669Z"
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "63dbf1d9deb67637af272748",
            "bookingId": 1435,
            "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
            "services": [
                {
                    "serviceCategory": "61f7a207e6bfed403ad9b79d",
                    "serviceName": "V-Day",
                    "serviceId": "6311c0ebe4cf75b15829f1a9",
                    "actualPrice": 800,
                    "discountedPrice": 520,
                    "quantity": 1,
                    "_id": "63dbf1d9deb67637af272737",
                    "createdAt": "2023-02-02T17:24:41.215Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak Singh",
                "zipcode": 201305,
                "phoneNumber": "+919415332242",
                "city": "Noida",
                "state": "Uttar Pradesh"
            },
            "serviceDate": "2023-01-01",
            "timeSlot": "01: 30 PM  -  02: 00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": true,
            "isCustomerCancelledService": false,
            "isAdminCancelledService": true,
            "finalPrice": 559,
            "cartAmount": 520,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "63adc234c182c881af2a8b44",
                "63c82cedc14c1d5b21f04077"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": false,
            "formattedTimestamp": "2023-01-28 00:02:25",
            "timeOfBooking": "2023-02-02T17:24:41.685Z",
            "createdAt": "2023-02-02T17:24:41.685Z",
            "approvedAt": "2023-02-02T17:24:41.685Z",
            "__v": 0,
            "adminCancellationReason": "Test",
            "adminCancelledServiceAt": "2023-02-03T20:13:40.645Z",
            "cancelledAt": "2023-02-03T20:13:40.645Z"
        },
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "amount": 39,
                "_id": "61f78c565575e8e5dfc0d438",
                "name": "Hygenic Fee",
                "createdAt": "2023-02-03T15:49:45.756Z"
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "63dd2d195770b3f95b67cb07",
            "bookingId": 1437,
            "serviceCategoryId": "61f7a207e6bfed403ad9b79d",
            "services": [
                {
                    "serviceCategory": "61f7a207e6bfed403ad9b79d",
                    "serviceName": "V-Day",
                    "serviceId": "6311c0ebe4cf75b15829f1a9",
                    "actualPrice": 800,
                    "discountedPrice": 520,
                    "quantity": 1,
                    "_id": "63dd2d195770b3f95b67caf6",
                    "createdAt": "2023-02-03T15:49:45.668Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak Singh",
                "zipcode": 201305,
                "phoneNumber": "+919415332242",
                "city": "Noida",
                "state": "Uttar Pradesh"
            },
            "serviceDate": "2023-01-01",
            "timeSlot": "01: 30 PM  -  02: 00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": true,
            "isCustomerCancelledService": false,
            "isAdminCancelledService": true,
            "finalPrice": 559,
            "cartAmount": 520,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "63adc234c182c881af2a8b44",
                "63c82cedc14c1d5b21f04077"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": false,
            "formattedTimestamp": "2023-02-03 00:35:09",
            "timeOfBooking": "2023-02-03T15:49:45.767Z",
            "createdAt": "2023-02-03T15:49:45.767Z",
            "approvedAt": "2023-02-03T15:49:45.767Z",
            "__v": 0,
            "adminCancellationReason": "Test",
            "adminCancelledServiceAt": "2023-02-03T20:13:32.150Z",
            "cancelledAt": "2023-02-03T20:13:32.150Z"
        },
        {
            "customer": {
                "name": "Deepak Singh",
                "email": "Web.dev.deepaksingh@gmail.com",
                "phoneNumber": "+919415332242"
            },
            "extraCharge": {
                "amount": 39,
                "_id": "61f78c565575e8e5dfc0d438",
                "name": "Hygenic Fee",
                "createdAt": "2023-01-21T08:01:13.774Z"
            },
            "bookingJourney": {
                "isStarted": false,
                "isStopped": false,
                "isCustomerPaid": false,
                "amountPaidByCustomer": 0
            },
            "_id": "63cb9bc9c92b75afe03e5c02",
            "bookingId": 1429,
            "serviceCategoryId": "61fc1329d40e07cb2b490823",
            "services": [
                {
                    "serviceCategory": "61fc1329d40e07cb2b490823",
                    "serviceName": "Haircut + Beard Trim",
                    "serviceId": "61fe1fdeff733d1fedf3860f",
                    "actualPrice": 459,
                    "discountedPrice": 349,
                    "quantity": 1,
                    "_id": "63cb9b36c92b75afe03e5beb",
                    "createdAt": "2023-01-21T07:58:46.290Z"
                }
            ],
            "customerId": "636e30e1ff17b27d5e9d7ef5",
            "address": {
                "name": "Deepak Singh",
                "phoneNumber": "9415332242",
                "zipcode": 201301,
                "city": "Noida",
                "state": "Uttar Pradesh",
                "coordinates": [
                    28.5906937,
                    77.3715315
                ],
                "landmark": "Sector 52",
                "houseNo": "1st Floor, "
            },
            "serviceDate": "2023-01-21",
            "timeSlot": "03:30 PM  -  04:00 PM",
            "modeOfPayment": "COD",
            "isPaid": false,
            "isServiceProviderAssigned": false,
            "isJobDone": false,
            "isRequestedToCancelService": false,
            "rating": 0,
            "isCancelled": false,
            "isCustomerCancelledService": false,
            "isAdminCancelledService": false,
            "finalPrice": 388,
            "cartAmount": 349,
            "isAdminApprovedCancellationRequest": false,
            "requestedServiceProviders": [
                "63c82cedc14c1d5b21f04077"
            ],
            "systemOrManual": 0,
            "isFeedbackGivenByCustomer": false,
            "formattedTimestamp": "2023-01-20 06:26:48",
            "timeOfBooking": "2023-01-21T08:01:13.799Z",
            "createdAt": "2023-01-21T08:01:13.799Z",
            "approvedAt": "2023-01-21T08:01:13.799Z",
            "__v": 0
        }
    ]
}
```