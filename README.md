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

3. GET Request
   - Goal: Get a user based on a valid ID.
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7177340
     - Method: GET
     - Authorization: Bearer Token
   - Expected Response:
     - Status Code: 200 Ok
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
   - Conclusion: Positive testing was successful. User data has been successfully retrieved based on ID.

4. PUT Request
   - Goal: Update user data on one property
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7177340
     - Method: GET
     - Authorization: Bearer Token
     - body:
```
       {
        "name": "Yani Apexindo",
        "email": "yani-apexindo@gmail.com",
        "gender": "female",
        "status": "inactive"
       }
```
    - Expected Response:
      - Status Code: 200 Ok
      - Response Body:
```
       {
        "name": "Yani Apexindo",
        "email": "yani-apexindo@gmail.com",
        "gender": "female",
        "status": "inactive",
        "id": 7177340
       }
```
   - Conclusion: Positive testing was successful. Update user data has been successfully on one property.

5. PATCH Request
   - Goal: Updated user data on three property
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7177340
     - Method: PATCH
     - Authorization: Bearer Token
     - body:
```
       {
        "name": "Tasha Red Apexindo",
        "email": "Tasha-Red-apexindo123@gmail.com",
        "gender": "male",
        "status": "inactive"
       }
```
   - Expected Response:
     - Status Code: 200 Ok
     - Response Body:
```
       {
        "name": "Tasha Red Apexindo",
        "email": "Tasha-Red-apexindo123@gmail.com",
        "gender": "male",
        "status": "inactive",
        "id": 7177340
       }
```
   - Conclusion: Positive testing was successful. Update user data has been successfully on three property.

5. DELETE Request
   - Goal: Delete user data with a valid ID
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7177340
     - Method: DELETE
     - Authorization: Bearer Token
   - Expected Response:
     - Status Code: 204 No Content
     - Response Body:
   - Conclusion: Positive testing was successful. Delete user data has been successfully with a valid ID.

## Negatif Testing
1. GET Request
   - Goal: Get all users based on not valid URL.
   - Request:
     - URL: https://gorest.co.in/public/v5/users
     - Method: GET
   - Expected Response:
     - Status Code: 404 Not Found
     - Response Body:
```
   <!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <meta content="width=device-width, initial-scale=1, shrink-to-fit=no" name="viewport" />
    <link href="/favicon.ico" rel="icon" type="image/x-icon" />
    <title>Page Not Found | GO REST</title>
    <meta name="csrf-param" content="authenticity_token" />
    <meta name="csrf-token"
        content="dYe3Ehl8UUsdOqAm-sJb4eIZAktww1DtPx48eVYfS32q6P4IKShCUsMmBDfFaHP_pvvpvxyqMb_wmMwUklYJpA" />
    <link rel="stylesheet"
        href="/assets/application-6286ef85f8dd095e49957bfc5b0cba0b68df3592774b35d0494027d130601970.css" media="all"
        data-turbolinks-track="reload" />
    <script src="/packs/js/application-194ed409298f13f197d2.js" data-turbolinks-track="reload" defer="defer"></script>
    <script async="true" crossorigin="anonymous"
        src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-4930099895671899"></script>
    <script async="true" src="https://www.googletagmanager.com/gtag/js?id=G-7KR6VNWHWS"></script>
    <script>
        window.dataLayer = window.dataLayer || [];function gtag(){dataLayer.push(arguments);}gtag('js', new Date());gtag('config', 'G-7KR6VNWHWS');
    </script>
</head>
```
      - Conclusion: Negative testing was successful. create a new user has been successfully with not a valid body.

2. POST
   - Goal: create a new user with not a valid body.
   - Request:
     - URL: https://gorest.co.in/public/v2/users
     - Method: POST
     - Authorization: Bearer Token
     - body:
```
       {
        "name": "Yani Apexindo",
        "email": "",
        "gender": "",
        "status": ""
       }
```
   - Expected Response:
     - Status Code: 422 Unprocessable Entity
     - Response Body:
```
[
       {
        "field": "email",
        "meassage": "can't be blank" 
       },
       {
        "field": "gender",
        "meassage": "can't be blank" 
       }
       {
        "field": "status",
        "meassage": "can't be blank" 
       }
]
```
   - Conclusion: Negative testing was successful. Create a new user has been succeessfully with not a valid body.

3. GET Request
   - Goal: Get a user based on not valid ID.
   - Request:
     - URL: https://gorest.co.in/public/v2/users/123
     - Method: GET
     - Authorization: Bearer Token
   - Expected Response:
     - Status Code: 404 Not Found
     - Response Body:
```
   {
   "message": Resource not found"
   }
```
   - Conclusion: Negative testing was successful. Get a user based on not valid ID has been succeessfully.

4. PUT Request
   - Goal: Update user data with empty value
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7167764
     - Method: PUT
     - Authorization: Bearer Token
   - Expected Response:
     - Status Code: 404 Not Found
     -   - body:
```
       {
        "status": ""
       }
```
   - Response Body:
```
   {
   "message": Resource not found"
   }
```
   - Conclusion: Negative testing was successful. Updated user data with empty value has been succeessfully.

5. PATCH Request
   - Goal: Update user data with empty values on two request parameters
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7141118
     - Method: PATCH
     - Authorization: Bearer Token
   - Expected Response:
     - Status Code: 400 Bad Request
     - body:
```
       {
        "status": ,
        "email":
       }
```
   - Response Body:
```
   {
   "message": "Error occurred while parsing request parameters"
   }
```
   - Conclusion: Negative testing was successful. Update user data with empty values on two request parameters hasbeen successfully.

5. DELETE Request
   - Goal: Delete user with non available ID
   - Request:
     - URL: https://gorest.co.in/public/v2/users/7167764
     - Method: DELETE
     - Authorization: Bearer Token
   - Expected Response:
     - Status Code: 404 Not Found
   - Response Body:
```
   {
   "message": "Resource not found"
   }
```
   - Conclusion: Negative testing was successful. Delete user with non exist ID has been succeessfully.
