# Endpoints_Auth Password Login Create

**Method:** POST
**URL:** `/api/v2//auth/password_login`

## Summary
Password Login | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//auth/password_login
Query Parametersformat stringPossible values: [json, xml]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredusernamestringrequiredPossible values: non-emptypasswordstringrequiredPossible values: non-emptydirect_auth_keystringrequiredPossible values: non-emptyverification_keystringnullablePossible values: non-emptyBodyrequiredusernamestringrequiredPossible values: non-emptypasswordstringrequiredPossible values: non-emptydirect_auth_keystringrequiredPossible values: non-emptyverification_keystringnullablePossible values: non-emptyBodyrequiredusernamestringrequiredPossible values: non-emptypasswordstringrequiredPossible values: non-emptydirect_auth_keystringrequiredPossible values: non-emptyverification_keystringnullablePossible values: non-empty
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaoneOfGetAccessTokenSuccessPendingLoginaccess_tokenstringrequiredexpires_inintegernullablerequiredrefresh_tokenstringrequiredobjectstringrequiredConstant value: pending_loginPossible values: [pending_login]idstring&lt;uuid&gt;requiredcreated_atstring&lt;date-time&gt;requireduserintegerrequiredtwo_factor_required_providersinteger[]required{  "access_token": "string",  "expires_in": 0,  "refresh_token": "string"}SchemaExample (auto)SchemaoneOfGetAccessTokenSuccessPendingLoginaccess_tokenstringrequiredexpires_inintegernullablerequiredrefresh_tokenstringrequiredobjectstringrequiredConstant value: pending_loginPossible values: [pending_login]idstring&lt;uuid&gt;requiredcreated_atstring&lt;date-time&gt;requireduserintegerrequiredtwo_factor_required_providersinteger[]required&lt;root&gt;  &lt;access_token&gt;string&lt;/access_token&gt;  &lt;expires_in&gt;0&lt;/expires_in&gt;  &lt;refresh_token&gt;string&lt;/refresh_token&gt;&lt;/root&gt;pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "username": "string",  "password": "string",  "direct_auth_key": "string",  "verification_key": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json'}conn.request("POST", "/api/v2/auth/password_login", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2ParametersShow optional parametersformat — query---jsonxmlBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"username": "string",
"password": "string",
"direct_auth_key": "string",
"verification_key": "string"
## Example Request / Response JSON
```json
{  "access_token": "string",  "expires_in": 0,  "refresh_token": "string"}
```

```json
{  "username": "string",  "password": "string",  "direct_auth_key": "string",  "verification_key": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json'}
```

```json
{
"username": "string",
"password": "string",
"direct_auth_key": "string",
"verification_key": "string"
}
```


