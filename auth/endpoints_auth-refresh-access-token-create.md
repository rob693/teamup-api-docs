# Endpoints_Auth Refresh Access Token Create

**Method:** POST
**URL:** `/api/v2//auth/refresh_access_token`

## Summary
Refresh Access Token | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//auth/refresh_access_token
Query Parametersformat stringPossible values: [json, xml]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredrefresh_tokenstringrequiredPossible values: non-emptyscopestring[]Possible values: non-emptynew_access_token_typestringThe type of the new access token. The TeamUp-Request-Mode header for requests made the new token must match this type.Possible values: [customer, provider]Default value: customerBodyrequiredrefresh_tokenstringrequiredPossible values: non-emptyscopestring[]Possible values: non-emptynew_access_token_typestringThe type of the new access token. The TeamUp-Request-Mode header for requests made the new token must match this type.Possible values: [customer, provider]Default value: customerBodyrequiredrefresh_tokenstringrequiredPossible values: non-emptyscopestring[]Possible values: non-emptynew_access_token_typestringThe type of the new access token. The TeamUp-Request-Mode header for requests made the new token must match this type.Possible values: [customer, provider]Default value: customer
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaaccess_tokenstringrequiredexpires_inintegernullablerequiredrefresh_tokenstringrequired{  "access_token": "string",  "expires_in": 0,  "refresh_token": "string"}SchemaExample (auto)Schemaaccess_tokenstringrequiredexpires_inintegernullablerequiredrefresh_tokenstringrequired&lt;root&gt;  &lt;access_token&gt;string&lt;/access_token&gt;  &lt;expires_in&gt;0&lt;/expires_in&gt;  &lt;refresh_token&gt;string&lt;/refresh_token&gt;&lt;/root&gt;pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "refresh_token": "string",  "scope": [    "string"  ],  "new_access_token_type": "customer"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json'}conn.request("POST", "/api/v2/auth/refresh_access_token", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2ParametersShow optional parametersformat — query---jsonxmlBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"refresh_token": "string",
"scope": [
"new_access_token_type": "customer"
## Example Request / Response JSON
```json
{  "access_token": "string",  "expires_in": 0,  "refresh_token": "string"}
```

```json
{  "refresh_token": "string",  "scope": [    "string"  ],  "new_access_token_type": "customer"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json'}
```

```json
{
"refresh_token": "string",
"scope": [
"string"
],
"new_access_token_type": "customer"
}
```


