# Endpoints_Customer Issues Retrieve

**Method:** GET
**URL:** `/api/v2//customer_issues/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customer_issues/:id
Path Parametersid integerrequiredA unique integer value identifying this case.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [customer_issue]namestringrequiredPossible values: &lt;= 256 characterscustomerintegerrequiredstatus integer ExpandablerequiredoneOfExpandableFieldobjectintegerThis field is EXPANDABLE.importancestringrequiredPossible values: [Flag on Profiles, Normal, Consider case closed]case_type object DeferredThis field is DEFERRED.namestringrequired{  "id": 0,  "name": "string",  "customer": 0,  "status": 0,  "case_type": {    "name": "string"  }}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [customer_issue]namestringrequiredPossible values: &lt;= 256 characterscustomerintegerrequiredstatus integer ExpandablerequiredoneOfExpandableFieldobjectintegerThis field is EXPANDABLE.importancestringrequiredPossible values: [Flag on Profiles, Normal, Consider case closed]case_type object DeferredThis field is DEFERRED.namestringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;customer&gt;0&lt;/customer&gt;  &lt;status&gt;0&lt;/status&gt;  &lt;case_type&gt;    &lt;name&gt;string&lt;/name&gt;  &lt;/case_type&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customer_issues/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousListNextCustomer Membership HoldsCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "customer": 0,  "status": 0,  "case_type": {    "name": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


