# Endpoints_Membership Terms Update

**Method:** PUT
**URL:** `/api/v2//membership_terms/`

## Summary
Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//membership_terms/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this membership terms.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredbase_termsstringrequiredPossible values: non-emptyBodyrequiredbase_termsstringrequiredPossible values: non-emptyBodyrequiredbase_termsstringrequiredPossible values: non-empty
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [membership_terms]membershipintegerrequiredplanintegernullablebase_termsstringrequired{  "id": 0,  "membership": 0,  "plan": 0,  "base_terms": "string"}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [membership_terms]membershipintegerrequiredplanintegernullablebase_termsstringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;membership&gt;0&lt;/membership&gt;  &lt;plan&gt;0&lt;/plan&gt;  &lt;base_terms&gt;string&lt;/base_terms&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "base_terms": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/membership_terms/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"base_terms": "string"
## Example Request / Response JSON
```json
{  "id": 0,  "membership": 0,  "plan": 0,  "base_terms": "string"}
```

```json
{  "base_terms": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"base_terms": "string"
}
```


