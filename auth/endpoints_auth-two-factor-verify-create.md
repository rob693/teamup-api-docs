# Endpoints_Auth Two Factor Verify Create

**Method:** POST
**URL:** `/api/v2//auth/two_factor/verify`

## Summary
Verify 2FA Code | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//auth/two_factor/verify
Query Parametersformat stringPossible values: [json, xml]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredphone_numberstringrequiredPossible values: non-empty and &lt;= 20 charactersverification_codestringrequiredPossible values: non-empty and &lt;= 6 charactersBodyrequiredphone_numberstringrequiredPossible values: non-empty and &lt;= 20 charactersverification_codestringrequiredPossible values: non-empty and &lt;= 6 charactersBodyrequiredphone_numberstringrequiredPossible values: non-empty and &lt;= 20 charactersverification_codestringrequiredPossible values: non-empty and &lt;= 6 characters
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemasuccessstringrequiredConstant value: TruePossible values: [true]messagestringrequiredverification_keystringrequiredPossible values: &lt;= 32 characters{  "success": true,  "message": "string",  "verification_key": "string"}SchemaExample (auto)SchemasuccessstringrequiredConstant value: TruePossible values: [true]messagestringrequiredverification_keystringrequiredPossible values: &lt;= 32 characters&lt;root&gt;  &lt;success&gt;true&lt;/success&gt;  &lt;message&gt;string&lt;/message&gt;  &lt;verification_key&gt;string&lt;/verification_key&gt;&lt;/root&gt;pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "phone_number": "string",  "verification_code": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json'}conn.request("POST", "/api/v2/auth/two_factor/verify", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2ParametersShow optional parametersformat — query---jsonxmlBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"phone_number": "string",
"verification_code": "string"
## Example Request / Response JSON
```json
{  "success": true,  "message": "string",  "verification_key": "string"}
```

```json
{  "phone_number": "string",  "verification_code": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json'}
```

```json
{
"phone_number": "string",
"verification_code": "string"
}
```


