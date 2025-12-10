# Endpoints_Events Join Waitlist Create

**Method:** POST
**URL:** `/api/v2//events/`

## Summary
Join Waitlist | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//events/:id/join_waitlist
Path Parametersid integerrequiredA unique integer value identifying this event.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [waitlist_spot]statusstringrequiredPossible values: [on_waitlist, spot_reserved, expired, rejected]added_atstring&lt;date-time&gt;requiredspot_reserved_atstring&lt;date-time&gt;requiredreserved_spot_expires_atstring&lt;date-time&gt;requiredpositioninteger DeferredThis field is DEFERRED.{  "id": 0,  "status": "on_waitlist",  "added_at": "2024-07-29T15:51:28.071Z",  "spot_reserved_at": "2024-07-29T15:51:28.071Z",  "reserved_spot_expires_at": "2024-07-29T15:51:28.071Z",  "position": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [waitlist_spot]statusstringrequiredPossible values: [on_waitlist, spot_reserved, expired, rejected]added_atstring&lt;date-time&gt;requiredspot_reserved_atstring&lt;date-time&gt;requiredreserved_spot_expires_atstring&lt;date-time&gt;requiredpositioninteger DeferredThis field is DEFERRED.&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;status&gt;on_waitlist&lt;/status&gt;  &lt;added_at&gt;2024-07-29T15:51:28.071Z&lt;/added_at&gt;  &lt;spot_reserved_at&gt;2024-07-29T15:51:28.071Z&lt;/spot_reserved_at&gt;  &lt;reserved_spot_expires_at&gt;2024-07-29T15:51:28.071Z&lt;/reserved_spot_expires_at&gt;  &lt;position&gt;0&lt;/position&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customer": 0})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/events/:id/join_waitlist", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customer": 0
## Example Request / Response JSON
```json
{  "id": 0,  "status": "on_waitlist",  "added_at": "2024-07-29T15:51:28.071Z",  "spot_reserved_at": "2024-07-29T15:51:28.071Z",  "reserved_spot_expires_at": "2024-07-29T15:51:28.071Z",  "position": 0}
```

```json
{  "customer": 0}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"customer": 0
}
```


