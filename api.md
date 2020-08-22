/rest/auth-via-call - url to auth 

request data 
{
    "phone_number":00000000000
} 

success response data if user new
{
    "status": true, 
    "data": {
        "ucaller_id":0000000
    }
}

success response if user already 
{
    "status": true,  
    "data": {
        "token": "some string"
    }
}

------------------------------------------------------------------------------------------------------------------------

/rest/recall-auth-via-call url to recall
 
request data
{
    "phone_number":000000000000, 
    "ucaller_id":000000
}

success response data 
{
    "status": true,
    "data": {
        "ucaller_id": 000000
    }
}

------------------------------------------------------------------------------------------------------------------------

/rest/confirm-auth-via-call url to confirm phone number

request data
{
    "phone_number":00000000000,
    "confirm_code":000000
}

success response data 
{
    "status": true, 
    "data": true
}

------------------------------------------------------------------------------------------------------------------------

/rest/registration url to registration 

request data
{
    "phone_number":00000000000, 
    "confirm_code": 0000, 
    "sex": "0", 
    "first_name": "some string", 
    "last_name": "some string",
    "birth_day": "0000-00-00"
}

#sex
#0 - male
#1- female 

success response data
{
    "status": true,
    "data": {
        "token": "some string"
    }
}

------------------------------------------------------------------------------------------------------------------------
COMMON

fail response data for all requests 

1) if one error 
{
    "status": false,
    "msg": "some string"
}

2) if many errors  
{
    "status": false, 
     "msg": [
        "some string",
        ............
    ]
}

all request data in json format and used http POST method
