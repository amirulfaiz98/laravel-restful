<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

## About Laravel Restful

    Domain name: https://mizi.monster


## Register
    
    POST /api/register

    {
        "success": true,
        "data": {
            "token": "token-value",
            "name": "Mizi"
        },
        "message": "User register successfully."
    }
    

## Login

    POST /oauth/token

    {
        "token_type": "Bearer",
        "expires_in": 31622397,
        "access_token": "access-token-value",
        "refresh_token": "refresh-token-value"
    }

## Index

    GET /api/products

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

    GET /api/products/2

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

    DELETE /api/products/2

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

