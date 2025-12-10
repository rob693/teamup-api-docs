# Endpoints_Auth Application Retrieve

**Method:** GET
**URL:** `/api/v2//auth/application`

## Summary
Authenticated Application | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//auth/application
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Client-ID stringID of the application
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequirednamestringPossible values: &lt;= 255 charactersobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [authenticated_application]scoped_providers object[]requiredArray [idintegerrequirednamestringrequiredPossible values: &lt;= 255 charactersobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [scoped_provider]]{  "id": 0,  "name": "string",  "scoped_providers": [    {      "id": 0,      "name": "string"    }  ]}SchemaExample (auto)SchemaidintegerrequirednamestringPossible values: &lt;= 255 charactersobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [authenticated_application]scoped_providers object[]requiredArray [idintegerrequirednamestringrequiredPossible values: &lt;= 255 charactersobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [scoped_provider]]&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;scoped_providers&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;  &lt;/scoped_providers&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/auth/application", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Client-ID — headerSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousRate LimitsNextCheck AccountCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "scoped_providers": [    {      "id": 0,      "name": "string"    }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


