# Endpoints_Bulk Actions Retrieve

**Method:** GET
**URL:** `/api/v2//bulk_actions/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//bulk_actions/:id
Path Parametersid stringrequiredQuery Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [bulk_action]typestringrequiredPossible values: &lt;= 128 charactersjob integer ExpandableoneOfExpandableFieldJobintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [job]result_urlstring&lt;uri&gt;requiredtotal_itemsintegerrequiredPossible values: &gt;= -2147483648 and &lt;= 2147483647complete_itemsintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647{  "id": 0,  "type": "string",  "job": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [bulk_action]typestringrequiredPossible values: &lt;= 128 charactersjob integer ExpandableoneOfExpandableFieldJobintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [job]result_urlstring&lt;uri&gt;requiredtotal_itemsintegerrequiredPossible values: &gt;= -2147483648 and &lt;= 2147483647complete_itemsintegerPossible values: &gt;= -2147483648 and &lt;= 2147483647&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;type&gt;string&lt;/type&gt;  &lt;job&gt;0&lt;/job&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/bulk_actions/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousBulk ActionsNextExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "type": "string",  "job": 0}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


