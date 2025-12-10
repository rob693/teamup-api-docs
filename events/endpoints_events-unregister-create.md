# Endpoints_Events Unregister Create

**Method:** POST
**URL:** `/api/v2//events/`

## Summary
Unregister | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//events/:id/unregister
Path Parametersid integerrequiredA unique integer value identifying this event.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemalatestringrequiredWhether the unregistering counted as a late cancel.attendanceintegerrequired{  "late": "string",  "attendance": 0}SchemaExample (auto)SchemalatestringrequiredWhether the unregistering counted as a late cancel.attendanceintegerrequired&lt;root&gt;  &lt;late&gt;string&lt;/late&gt;  &lt;attendance&gt;0&lt;/attendance&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customer": 0,  "is_late_cancel": True})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/events/:id/unregister", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customer": 0,
"is_late_cancel": true
## Example Request / Response JSON
```json
{  "late": "string",  "attendance": 0}
```

```json
{  "customer": 0,  "is_late_cancel": True}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"customer": 0,
"is_late_cancel": true
}
```


