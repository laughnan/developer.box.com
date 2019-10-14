---
rank: 20
alias_paths:
  - /docs/application-setup
cId: authentication
scId: null
id: authentication
isIndex: true
---

# Authentication

Authentication with the Box API uses an Access Token to identify a user. The
way in which an Access Token is acquired depends on the method used to authorize
a user. The type of authorization available to an application depends on the
use-case as well as the type of application that has been created in the developer
console.

| Box Application Type   | Authorization methods                         |
| ---------------------- | --------------------------------------------- |
| Custom App             | [OAuth 2.0][oauth2], [JWT][jwt], or App token |
| Enterprise Integration | [OAuth 2.0][oauth2], [JWT][jwt]               |
| Partner Integration    | App token                                     |
| Custom Skill           | No authorization needed                       |

<CTA to="guide://authentication/select">
  Learn how to select an authorization type

</CTA>

## Access Tokens for Authentication

Every API endpoint requires a valid and active **Access Token** to make API
calls. An Access Token is a unique string that identifies an authenticated Box
user to the API endpoints.

```curl
curl https://api.box.com/2.0/users/me \
  -H "Authorization: Bearer EGmDmRVfhfHsqesn5yVYHAqUkD0dyDfk"
```

## User Authorization

There are a few ways to get an an Access Token for a user. There is
client-side authorization through [OAuth 2.0][oauth2], server-side authorization
using [JWT][jwt], as well as a long lived App Token and a short-lived Developer
Token.

[oauth2]: guide://authentication/oauth2
[jwt]: guide://authentication/jwt