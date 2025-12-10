# Endpoints_Family Invites Create

**Method:** POST
**URL:** `/api/v2//family_invites`

## Summary
Create | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//family_invites
Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredfirst_namestringrequiredPossible values: non-empty and &lt;= 256 characterslast_namestringrequiredPossible values: non-empty and &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: non-empty and &lt;= 254 charactersBodyrequiredfirst_namestringrequiredPossible values: non-empty and &lt;= 256 characterslast_namestringrequiredPossible values: non-empty and &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: non-empty and &lt;= 254 charactersBodyrequiredfirst_namestringrequiredPossible values: non-empty and &lt;= 256 characterslast_namestringrequiredPossible values: non-empty and &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: non-empty and &lt;= 254 characters
Responses​201application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [family_invite]first_namestringrequiredPossible values: &lt;= 256 characterslast_namestringrequiredPossible values: &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: &lt;= 254 charactersclaim_urlstringrequiredclaimed_byintegernullable{  "id": 0,  "first_name": "string",  "last_name": "string",  "email": "user@example.com",  "claim_url": "string",  "claimed_by": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [family_invite]first_namestringrequiredPossible values: &lt;= 256 characterslast_namestringrequiredPossible values: &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: &lt;= 254 charactersclaim_urlstringrequiredclaimed_byintegernullable&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;first_name&gt;string&lt;/first_name&gt;  &lt;last_name&gt;string&lt;/last_name&gt;  &lt;email&gt;user@example.com&lt;/email&gt;  &lt;claim_url&gt;string&lt;/claim_url&gt;  &lt;claimed_by&gt;0&lt;/claimed_by&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "first_name": "string",  "last_name": "string",  "email": "user@example.com"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/family_invites", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"first_name": "string",
"last_name": "string",
"email": "user@example.com"
## Example Request / Response JSON
```json
{  "id": 0,  "first_name": "string",  "last_name": "string",  "email": "user@example.com",  "claim_url": "string",  "claimed_by": 0}
```

```json
{  "first_name": "string",  "last_name": "string",  "email": "user@example.com"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"first_name": "string",
"last_name": "string",
"email": "user@example.com"
}
```


