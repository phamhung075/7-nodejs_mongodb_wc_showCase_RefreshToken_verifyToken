# Node.js MongoDB Showcase Projects

This is a personal project series based on the lessons by @anonystick ([https://github.com/anonystick](https://github.com/anonystick)).
## 1. [Authentication and API Key Management (HS256)](https://github.com/phamhung075/2-nodejs_mongodb_wc_showCase_Dynamic_for_ApiKey_and_Permissions_HS256/tree/master)

## 2. [ErrorHandler ApiResponse](https://github.com/phamhung075/3-nodejs_mongodb_wc_showCase_ErrorHandler_API)

## 3. [Success Handler ApiResponse](https://github.com/phamhung075/4-nodejs_mongodb_wc_showCase_ApiResponseUseClass/tree/master?tab=readme-ov-file)

## 4. [SignUp and Login Public Access](https://github.com/phamhung075/5-nodejs_mongodb_wc_showCase_SignUpLogin)

## 5. [Logout Authentication](https://github.com/phamhung075/6-nodejs_mongodb_wc_showCase_LogoutAuthentication/tree/master)
## 6. Refresh Token and Token Verification

### Introduction

`7-nodejs_mongodb_wc_showCase_RefreshToken_verifyToken` is a Node.js application that enhances user authentication with refresh token functionality and token verification, using MongoDB. This project builds upon previous work to provide a more secure and robust authentication system.

### Installation
 
    `git clone https://github.com/phamhung075/7-nodejs_mongodb_wc_showCase_RefreshToken_verifyToken.git`
    
- Change to the directory:

    `cd 7-nodejs_mongodb_wc_showCase_RefreshToken_verifyToken`
    
- Install dependencies:
  
    `npm install`
    

### Features

- **Access Service** (`./services/access.service.js`): Manages user authentication, including handling of refresh tokens and token verification.
- **KeyToken Service** (`./services/keyToken.service.js`): Responsible for token creation, validation, and management.
- **Models**:
    - **KeyToken Model** (`./models/keyToken.model.js`): Schema for key tokens.
- **Controllers**:
    - **Access Controller** (`./controllers/access.controller.js`): Orchestrates user authentication routes, including token management.
- **Helpers**:
    - **Async Handler** (`./helpers/asyncHandle.js`): Assists with handling asynchronous operations.

### Usage

- Demonstrates advanced user authentication with refresh token mechanisms and token verification.
- MongoDB Connection: `mongodb://localhost:27017`

### Postman Examples

- **Signup**, **Login**, **Logout** examples as in the previous project.
- **Token Refresh** 

``` 
@url_dev=http://localhost:3052/v1/api/

### logout
POST {{url_dev}}/shop/handlerRefreshToken
Content-Type: application/json
x-api-key: [API_KEY]
x-client-id: [SHOP_ID]
x-rtoken-id: [REFRESH_TOKEN]
```
