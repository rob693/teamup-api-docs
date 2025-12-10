# Endpoints_Customers Sms Account Verify Create

**Method:** POST
**URL:** `/api/v2//customers/`

## Summary
Verify SMS Account | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//customers/:id/sms_account/verify
Path Parametersid integerrequiredA unique integer value identifying this provider customer profile.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyverification_codestringnullablePossible values: non-empty and &lt;= 8 charactersBodyverification_codestringnullablePossible values: non-empty and &lt;= 8 charactersBodyverification_codestringnullablePossible values: non-empty and &lt;= 8 characters
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemastatusstringrequiredConstant value: OKPossible values: [OK]{  "status": "OK"}SchemaExample (auto)SchemastatusstringrequiredConstant value: OKPossible values: [OK]&lt;status&gt;OK&lt;/status&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "verification_code": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/customers/:id/sms_account/verify", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"verification_code": "string"
## Example Request / Response JSON
```json
{  "status": "OK"}
```

```json
{  "verification_code": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"verification_code": "string"
}
```


