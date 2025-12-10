# Endpoints_Crm Workflows Create

**Method:** POST
**URL:** `/api/v2//crm/workflows`

## Summary
Create | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//crm/workflows
Must have one of the following permissions: super_admin.
Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequirednamestringnullablePossible values: non-empty and &lt;= 255 characterstriggerstringrequired
Possible values: [lead_form.submitted]BodyrequirednamestringnullablePossible values: non-empty and &lt;= 255 characterstriggerstringrequired
Possible values: [lead_form.submitted]BodyrequirednamestringnullablePossible values: non-empty and &lt;= 255 characterstriggerstringrequired
Possible values: [lead_form.submitted]
Responses​201application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [crm_workflow]namestringnullablePossible values: &lt;= 255 characterstriggerstringrequired
Possible values: [lead_form.submitted]{  "id": 0,  "name": "string",  "trigger": "lead_form.submitted"}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [crm_workflow]namestringnullablePossible values: &lt;= 255 characterstriggerstringrequired
Possible values: [lead_form.submitted]&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;trigger&gt;lead_form.submitted&lt;/trigger&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "name": "string",  "trigger": "lead_form.submitted"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/crm/workflows", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "trigger": "lead_form.submitted"}
```

```json
{  "name": "string",  "trigger": "lead_form.submitted"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"trigger": "lead_form.submitted"
}
```


