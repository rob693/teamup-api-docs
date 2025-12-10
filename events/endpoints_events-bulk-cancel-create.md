# Endpoints_Events Bulk Cancel Create

**Method:** POST
**URL:** `/api/v2//events/bulk_cancel`

## Summary
Bulk Cancel | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//events/bulk_cancel
Must have one of the following permissions: super_admin, manage_events.
Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [bulk_action]typestringrequiredPossible values: &lt;= 128 charactersjob integer ExpandableoneOfExpandableFieldJobintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [job]result_urlstring&lt;uri&gt;requiredtotal_itemsintegerrequiredPossible values: &gt;= -2147483648 and &lt;= 2147483647complete_itemsintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647{  "id": 0,  "type": "string",  "job": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [bulk_action]typestringrequiredPossible values: &lt;= 128 charactersjob integer ExpandableoneOfExpandableFieldJobintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [job]result_urlstring&lt;uri&gt;requiredtotal_itemsintegerrequiredPossible values: &gt;= -2147483648 and &lt;= 2147483647complete_itemsintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;type&gt;string&lt;/type&gt;  &lt;job&gt;0&lt;/job&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "events": {}})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/events/bulk_cancel", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"events": {}
## Example Request / Response JSON
```json
{  "id": 0,  "type": "string",  "job": 0}
```

```json
{  "events": {}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"events": {}
```


