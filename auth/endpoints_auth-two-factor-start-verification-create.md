# Endpoints_Auth Two Factor Start Verification Create

**Method:** POST
**URL:** `/api/v2//auth/two_factor/start_verification`

## Summary
Start 2FA Verification | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//auth/two_factor/start_verification
Query Parametersformat stringPossible values: [json, xml]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredphone_numberstringrequiredPossible values: non-empty and &lt;= 20 charactersproviderintegerrequireddirect_auth_keystringrequiredPossible values: non-emptypending_loginstring&lt;uuid&gt;nullableBodyrequiredphone_numberstringrequiredPossible values: non-empty and &lt;= 20 charactersproviderintegerrequireddirect_auth_keystringrequiredPossible values: non-emptypending_loginstring&lt;uuid&gt;nullableBodyrequiredphone_numberstringrequiredPossible values: non-empty and &lt;= 20 charactersproviderintegerrequireddirect_auth_keystringrequiredPossible values: non-emptypending_loginstring&lt;uuid&gt;nullable
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemasuccessstringrequiredConstant value: TruePossible values: [true]messagestringrequiredexpires_atstring&lt;date-time&gt;verification_codestringPossible values: &lt;= 6 characters{  "success": true,  "message": "string",  "expires_at": "2024-07-29T15:51:28.071Z",  "verification_code": "string"}SchemaExample (auto)SchemasuccessstringrequiredConstant value: TruePossible values: [true]messagestringrequiredexpires_atstring&lt;date-time&gt;verification_codestringPossible values: &lt;= 6 characters&lt;root&gt;  &lt;success&gt;true&lt;/success&gt;  &lt;message&gt;string&lt;/message&gt;  &lt;expires_at&gt;2024-07-29T15:51:28.071Z&lt;/expires_at&gt;  &lt;verification_code&gt;string&lt;/verification_code&gt;&lt;/root&gt;pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "phone_number": "string",  "provider": 0,  "direct_auth_key": "string",  "pending_login": "3fa85f64-5717-4562-b3fc-2c963f66afa6"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json'}conn.request("POST", "/api/v2/auth/two_factor/start_verification", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2ParametersShow optional parametersformat — query---jsonxmlBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"phone_number": "string",
"provider": 0,
"direct_auth_key": "string",
"pending_login": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
## Example Request / Response JSON
```json
{  "success": true,  "message": "string",  "expires_at": "2024-07-29T15:51:28.071Z",  "verification_code": "string"}
```

```json
{  "phone_number": "string",  "provider": 0,  "direct_auth_key": "string",  "pending_login": "3fa85f64-5717-4562-b3fc-2c963f66afa6"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json'}
```

```json
{
"phone_number": "string",
"provider": 0,
"direct_auth_key": "string",
"pending_login": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
}
```


