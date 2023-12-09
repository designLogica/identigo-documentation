---
title: 01. Architecture
---
# Architecture

Identigo is pretty simple really, there are apps and there are users.

##### Users can belong to many apps
Users then have roles and attributes assigned to them for each app.

##### Apps have roles and attributes
Only roles and attributes configured on the app can be assigned to a user of that app.

## Types of login

Each app can have different types of login turned on or off.
There are 5 types of login available at the current time.

* Username and Password
* Passwordless via email
* Username and Password, with OTP
    * Email or SMS
* Username and Password with MFA
    * Authenticator app
* Webauthn

These options can be turned on in the app admin section.

## Login flow

When a user logs in, there is a secure cookie set on the identigo server domain, when they are redirected we send back a request token which gets exchanged for a real token that gets stored as a cookie in your app domain.

If a user tries to login again but their session is still valid, they will just get redirected.

If a user is a member of more than 1 app, Identigo will act as an SSO for those apps. For example, a user logs in to app 1, they then go to app 2 and click login, they will be instantly redirected back to app 2 and a request token will be exchanged.