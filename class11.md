# Code 301 Reading Notes

## Class 11

[<== Previous Lesson](class10.md) [Next Lesson ==>](class12.md)

[<== Home](README.md) 🏠

# Authentication

> OAuth allows websites and services to share assets among users.

## OAuth definition

OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

Example: Using google or github accounts as authentication for access to a third parrty service.

> The [OAuth 2.0](https://tools.ietf.org/html/rfc6749) authorization framework is a protocol that allows a user to grant a third-party web site or application access to the user's protected resources, without necessarily revealing their long-term credentials or even their identity.
>
> (...)
>
> Auth0 generates access tokens for API authorization scenarios, in [JSON web token (JWT) format](https://auth0.com/docs/tokens/json-web-tokens/json-web-token-structure). The permissions represented by the access token, in OAuth terms, are known as [scopes](https://auth0.com/docs/scopes). When an application authenticates with Auth0, it specifies the scopes it wants. If those scopes are authorized by the user, then the access token will represent these authorized scopes. *[-resource](https://auth0.com/docs/protocols/protocol-oauth2)*

An OAuth 2.0 flow has the following roles:

* **Resource Owner** : Entity that can grant access to a protected resource. Typically, this is the end-user.
* **Resource Server** : Server hosting the protected resources. This is the API you want to access.
* **Client** : Application requesting access to a protected resource on behalf of the Resource Owner.
* **Authorization Server** : Server that authenticates the Resource Owner and issues access tokens after getting proper authorization. In this case, Auth0.

> OAuth 2.0 defines four flows to get an access token. These flows are called grant types.

* [Authorization Code Flow](https://auth0.com/docs/flows/authorization-code-flow): used by Web Apps executing on a server. This is also used by mobile apps, using the [Proof Key for Code Exchange (PKCE) technique](https://auth0.com/docs/flows/authorization-code-flow-with-proof-key-for-code-exchange-pkce).
* [Implicit Flow with Form Post](https://auth0.com/docs/flows/implicit-flow-with-form-post): used by JavaScript-centric apps (Single-Page Applications) executing on the user's browser.
* [Resource Owner Password Flow](https://auth0.com/docs/flows/resource-owner-password-flow): used by highly-trusted apps.
* [Client Credentials Flow](https://auth0.com/docs/flows/client-credentials-flow): used for machine-to-machine communication.

### Endpoints

`/authorize` and `/oauth/token`

The request parameters of the `/authorize` endpoint are:


| Parameter       | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `response_type` | Tells the authorization server which grant to execute.                                                                                                                                                                                                                                                                                                                                                      |
| `response_mode` | (Optional) How the result of the authorization request is formatted. Values:<br/>- `query`: for Authorization Code grant. `302 Found` triggers redirect.<br/>- `fragment`: for Implicit grant. `302 Found` triggers redirect.<br/>- `form_post`: `200 OK` with response parameters embedded in an HTML form as hidden parameters.<br/>- `web_message`: For Silent Authentication. Uses HTML5 web messaging. |
| `client_id`     | The ID of the application that asks for authorization.                                                                                                                                                                                                                                                                                                                                                      |
| `redirect_uri`  | Holds a URL. A successful response from this endpoint results in a redirect to this URL.                                                                                                                                                                                                                                                                                                                    |
| `scope`         | A space-delimited list of permissions that the application requires.                                                                                                                                                                                                                                                                                                                                        |
| `state`         | An opaque value, used for security purposes. If this request parameter is set in the request, then it is returned to the application as part of the`redirect_uri`.                                                                                                                                                                                                                                          |

This endpoint is used by the Authorization Code and the Implicit grant types. The authorization server needs to know which grant type the application wants to use since it affects the kind of credential it will issue:

* For the Authorization Code grant, it will issue an authorization code (which can later be exchanged with an access token). = `response_type=code`
* For the Implicit grant, it will issue an access token. = `response_type=token` alternatively `response_type=id_token token` to include both an access token and an ID token.

> The OAuth 2.0 Multiple Response Type Encoding Practices specification added a parameter that specifies how the result of the authorization request is formatted. This parameter is called `response_mode`.

It is optional and can take the following values:


| Value         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `query`       | This is the default for Authorization Code grant. A successful response is`302 Found` which triggers a redirect to the `redirect_uri`. The response parameters are embedded in the query component (the part after `?`) of the `redirect_uri` in the `Location` header.<br/>For example:<br/>`HTTP/1.1 302 Found`<br/>`Location: https://my-redirect-uri.callback?code=js89p2x1` where the authorization ocde is `js89p21`.                                                                                                              |
| `fragment`    | This is the default for Implicit grant. A successful response is`302 Found`, which triggers a redirect to the `redirect_uri` (which is a request parameter). The response parameters are embedded in the fragment component (the part after `#`) of the `redirect_uri` in the `Location` header.<br/>For example:<br/>`HTTP/1.1 302 Found`<br/>`Location: https://my-redirect-uri/callback#access_token=eyB...78f&token_type=Bearer&expires_in=3600`.                                                                                    |
| `form_post`   | The response mode is defined by the[OAuth 2.0 Form Post Response Mode specification](https://openid.net/specs/oauth-v2-form-post-response-mode-1_0.html). A successful response is `200 OK` and the parameters are embedded in an HTML form as hidden params. The `action` of the form is the `redirect_uri` and the `onload` attribute is configured to submit the form. After the HTML is loaded by the browser, a redirect to the `redirect_uri` is done.                                                                             |
| `web_message` | This response mode is defined in[OAuth 2.0 Web Message Response Mode specification](https://tools.ietf.org/html/draft-sakimura-oauth-wmrm-00). It uses HTML5 Web Messaging instead of the redirect for the authorization response from the /authorization endpoint. This is particularly useful when using Silent Authentication. To do this response mode, you must register your app's URL at the **Allowed Web Origins** field in your Auth0 [application settings](https://manage.auth0.com/#/applications/YOUR_CLIENT_ID/settings). |

### Token endpoint

The `/oauth/token` endpoint is used by the application in order to get an access token or a refresh token. It is used by all flows except for the Implicit Flow because in that case an access token is issued directly.


# Auth0 React SDK for Single Page Apps

> bootstrap for authentication!

## Installation

You have a few options for using auth0-react.js in your project.

* From the CDN: `<script src="https://cdn.auth0.com/js/auth0-react/1.2.0/auth0-react.min.js"></script>`
* From [npm](https://npmjs.org/):
  `npm install @auth0/auth0-react`
* From [yarn](https://yarnpkg.com/): `yarn add @auth0/auth0-react`


### Reading

* [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)
* [Authorization and Authentication flows](https://auth0.com/docs/flows)

### Bookmark/Skim

* [Auth0 for single page apps](https://auth0.com/docs/libraries/auth0-react)

[<== Home](README.md) 🏠
