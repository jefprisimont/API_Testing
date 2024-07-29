## Introduction
This report aims to document the results of API testing on the https://gorest.co.in/public/v2/users endpoint. Testing is performed to ensure that each endpoint functions properly and returns the expected response. This test covers positive and negative scenarios for GET, POST, PUT, PATCH, and DELETE.

## Methodology
Testing is carried out with the following steps:
1. Define test scenarios.
2. Compile requests in Postman.
3. Execute requests and check responses.
4. Record test results.

## Positive Testing
1. GET (list users)
   - Goal: Get all users based on a valid ID.
   - Request:
     - URL: https://gorest.co.in/public/v2/users
     - Method: GET
   - Expected Response:
     - Status Code: 200 OK
     - Response Body:
```
     [
    {
        "id": 7167435,
        "name": "Mrs. Swarnalata Namboothiri",
        "email": "swarnalata_mrs_namboothiri@kuhn.test",
        "gender": "male",
        "status": "active"
    },
    {
        "id": 7167434,
        "name": "Mahendra Agarwal",
        "email": "mahendra_agarwal@hilll.example",
        "gender": "male",
        "status": "inactive"
    },
    {
        "id": 7167433,
        "name": "Aasa Guha",
        "email": "guha_aasa@durgan-kub.test",
        "gender": "male",
        "status": "active"
    },
    {
        "id": 7167432,
        "name": "Chidaatma Desai",
        "email": "desai_chidaatma@rice-marks.test",
        "gender": "female",
        "status": "inactive"
    },
    {
        "id": 7167431,
        "name": "Vedanga Kaniyar PhD",
        "email": "vedanga_kaniyar_phd@legros.test",
        "gender": "male",
        "status": "active"
    },
    {
        "id": 7167430,
        "name": "Nanda Rana",
        "email": "nanda_rana@feeney.example",
        "gender": "male",
        "status": "inactive"
    },
    {
        "id": 7167429,
        "name": "Buddhana Bharadwaj",
        "email": "bharadwaj_buddhana@ohara.example",
        "gender": "female",
        "status": "inactive"
    },
    {
        "id": 7167428,
        "name": "Pran Prajapat PhD",
        "email": "phd_prajapat_pran@kris.test",
        "gender": "female",
        "status": "inactive"
    },
    {
        "id": 7167427,
        "name": "Malati Mishra",
        "email": "malati_mishra@schneider.example",
        "gender": "male",
        "status": "inactive"
    },
    {
        "id": 7167426,
        "name": "Kanak Nair Sr.",
        "email": "nair_sr_kanak@hane.test",
        "gender": "male",
        "status": "inactive"
    }
]
```
   - Conclusion: Positive testing was successful. User data has been successfully retrieved based on valid ID.

2. POST
   - Goal: create a new user with valid data.
   - Request:
     - URL: https://gorest.co.in/public/v2/users
     - Method: POST
     - Authorization: Bearer Token
     - body:
```
       {
        "name": "Yani Apexindo",
        "email": "yani-apexindo@gmail.com",
        "gender": "female",
        "status": "active"
       }
```
   - Expected Response:
     - Status Code: 201 Created
     - Response Body:
```
       {
        "id": 7177340,
        "name": "Yani Apexindo",
        "email": "yani-apexindo@gmail.com",
        "gender": "female",
        "status": "active"
       }
```
   - Conclusion: Positive testing was successful. New user data has been successfully create with ID.

3. 


