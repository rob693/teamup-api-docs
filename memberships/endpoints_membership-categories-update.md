# Endpoints_Membership Categories Update

**Method:** PUT
**URL:** `/api/v2//membership_categories/`

## Summary
Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//membership_categories/:id
Must have one of the following permissions: customers.
Path Parametersid integerrequiredA unique integer value identifying this membership category.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequirednameCategory Name (string)requiredPossible values: non-empty and &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647BodyrequirednameCategory Name (string)requiredPossible values: non-empty and &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647BodyrequirednameCategory Name (string)requiredPossible values: non-empty and &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [membership_category]nameCategory Name (string)requiredPossible values: &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647{  "id": 0,  "name": "string",  "order": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [membership_category]nameCategory Name (string)requiredPossible values: &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;order&gt;0&lt;/order&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "name": "string",  "order": 0})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/membership_categories/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"name": "string",
"order": 0
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "order": 0}
```

```json
{  "name": "string",  "order": 0}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"order": 0
}
```


