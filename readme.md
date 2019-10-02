<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

# About Laravel Restful

    Domain name: https://mizi.monster

## Installation

    git clone
    composer update
    php artisan migrate
    php artisan passport:install


## Register
    
    POST /api/register

     {
        "name": "name", 
        "email": "email@email.com", 
        "password": "password", 
        "c_password": "password"   
    }

    Response

    {
        "success": true,
        "data": {
            "token": "token-value",
            "name": "name"
        },
        "message": "User register successfully."
    }
    

## Login

    POST /oauth/token

    Body
        username
        password
        grant_type
        client_id
        client_secret

    Response

    {
        "token_type": "Bearer",
        "expires_in": 31622397,
        "access_token": "access-token-value",
        "refresh_token": "refresh-token-value"
    }

## Index

    GET /api/products

    Headers
        Authorization
        Accept
    
    Response

    {
        "success": true,
        "data": [
            {
                "id": 1,
                "name": "Old Book",
                "detail": "First Version",
                "created_at": "2019-09-30 07:19:48",
                "updated_at": "2019-09-30 07:19:48"
            }
        ],
        "message": "Products retrieved successfully."
    }

## Store

    POST /api/products

    Headers
        Authorization
        Accept

    Body
        name
        detail

    Response

    {
        "success": true,
        "data": {
            "name": "New Book",
            "detail": "Second Version",
            "updated_at": "2019-10-01 17:20:23",
            "created_at": "2019-10-01 17:20:23",
            "id": 3
        },
        "message": "Product created successfully."
    }

## Show

    GET /api/products/{id}

    Headers
        Authorization
        Accept

    Response

    {
        "success": true,
        "data": {
            "id": 2,
            "name": "New Book",
            "detail": "Second Version",
            "created_at": "2019-09-30 07:19:48",
            "updated_at": "2019-09-30 07:19:48"
        },
        "message": "Product retrieved successfully."
    }

## Update

    PUT /api/products/2?name=NewBook&detail=NewVersion

    Headers
        Authorization
        Accept

    String Query
        name
        detail

    Response

    {
        "success": true,
        "data": {
            "id": 2,
            "name": "NewBook",
            "detail": "NewVersion",
            "created_at": "2019-09-30 07:19:48",
            "updated_at": "2019-10-01 17:23:13"
        },
        "message": "Product updated successfully."
    }

## Delete

    DELETE /api/products/{id}

    Headers
        Authorization
        Accept

    {
        "success": true,
        "data": {
            "id": 2,
            "name": "NewBook",
            "detail": "NewVersion",
            "created_at": "2019-10-01 17:20:23",
            "updated_at": "2019-10-01 17:20:23"
        },
        "message": "Product deleted successfully."
    }

