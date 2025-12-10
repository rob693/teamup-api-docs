# Endpoints_Membership Categories Create

**Method:** POST
**URL:** `/api/v2//membership_categories`

## Summary
Create | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//membership_categories
Must have one of the following permissions: customers.
Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredproviderstringnullablenameCategory Name (string)requiredPossible values: non-empty and &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647BodyrequiredproviderstringnullablenameCategory Name (string)requiredPossible values: non-empty and &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647BodyrequiredproviderstringnullablenameCategory Name (string)requiredPossible values: non-empty and &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647
Responses​201application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [membership_category]nameCategory Name (string)requiredPossible values: &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647{  "id": 0,  "name": "string",  "order": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [membership_category]nameCategory Name (string)requiredPossible values: &lt;= 256 charactersorderintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;order&gt;0&lt;/order&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "provider": "string",  "name": "string",  "order": 0})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/membership_categories", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"provider": "string",
"name": "string",
"order": 0
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "order": 0}
```

```json
{  "provider": "string",  "name": "string",  "order": 0}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"provider": "string",
"name": "string",
"order": 0
}
```


