# Endpoints_Crm Lead Forms Partial Update

**Method:** PATCH
**URL:** `/api/v2//crm/lead_forms/`

## Summary
Partially Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//crm/lead_forms/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this lead form.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodynamestringPossible values: non-empty and &lt;= 255 charactersdescriptionstringnullablePossible values: non-emptylead_sourceintegernullableredirect_urlstring&lt;uri&gt;nullableURL to redirect to after form submissionPossible values: &lt;= 200 characterssend_invite_emailbooleancustomer_fields object[]Array [customer_fieldintegerrequired]BodynamestringPossible values: non-empty and &lt;= 255 charactersdescriptionstringnullablePossible values: non-emptylead_sourceintegernullableredirect_urlstring&lt;uri&gt;nullableURL to redirect to after form submissionPossible values: &lt;= 200 characterssend_invite_emailbooleancustomer_fields object[]Array [customer_fieldintegerrequired]BodynamestringPossible values: non-empty and &lt;= 255 charactersdescriptionstringnullablePossible values: non-emptylead_sourceintegernullableredirect_urlstring&lt;uri&gt;nullableURL to redirect to after form submissionPossible values: &lt;= 200 characterssend_invite_emailbooleancustomer_fields object[]Array [customer_fieldintegerrequired]
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [lead_form]uuidstring&lt;uuid&gt;requirednamestringrequiredPossible values: &lt;= 255 charactersdescriptionstringnullablelead_source integer ExpandableoneOfExpandableFieldLeadSourceintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [lead_source]namestringrequiredPossible values: &lt;= 255 charactersarchivedbooleanredirect_urlstring&lt;uri&gt;nullableURL to redirect to after form submissionPossible values: &lt;= 200 characterssend_invite_emailboolean{  "id": 0,  "uuid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",  "name": "string",  "description": "string",  "lead_source": 0,  "redirect_url": "string",  "send_invite_email": true}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [lead_form]uuidstring&lt;uuid&gt;requirednamestringrequiredPossible values: &lt;= 255 charactersdescriptionstringnullablelead_source integer ExpandableoneOfExpandableFieldLeadSourceintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [lead_source]namestringrequiredPossible values: &lt;= 255 charactersarchivedbooleanredirect_urlstring&lt;uri&gt;nullableURL to redirect to after form submissionPossible values: &lt;= 200 characterssend_invite_emailboolean&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;uuid&gt;3fa85f64-5717-4562-b3fc-2c963f66afa6&lt;/uuid&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;description&gt;string&lt;/description&gt;  &lt;lead_source&gt;0&lt;/lead_source&gt;  &lt;redirect_url&gt;string&lt;/redirect_url&gt;  &lt;send_invite_email&gt;true&lt;/send_invite_email&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "name": "string",  "description": "string",  "lead_source": 0,  "redirect_url": "string",  "send_invite_email": True,  "customer_fields": [    {      "customer_field": 0    }  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/crm/lead_forms/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"name": "string",
"description": "string",
"lead_source": 0,
"redirect_url": "string",
"send_invite_email": true,
## Example Request / Response JSON
```json
{  "id": 0,  "uuid": "3fa85f64-5717-4562-b3fc-2c963f66afa6",  "name": "string",  "description": "string",  "lead_source": 0,  "redirect_url": "string",  "send_invite_email": true}
```

```json
{  "name": "string",  "description": "string",  "lead_source": 0,  "redirect_url": "string",  "send_invite_email": True,  "customer_fields": [    {      "customer_field": 0    }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"description": "string",
"lead_source": 0,
"redirect_url": "string",
"send_invite_email": true,
"customer_fields": [
{
"customer_field": 0
}
```


