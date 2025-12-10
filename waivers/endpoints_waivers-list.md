# Endpoints_Waivers List

**Method:** GET
**URL:** `/api/v2//waivers`

## Summary
List | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//waivers
Query Parametersapplicable_to string[]Possible values: [all_offering_types, all_memberships]expand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]page integerA page number within the paginated result set.page_size integerPossible values: &lt;= 100Number of results to return per page.status integerPossible values: [0, 2]
Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [idintegerrequirednamestringrequiredtextstringrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [waiver]statusstringrequiredPossible values: [Active, Archived]when_requiredstring[]requiredPossible values: [signup, all_memberships, all_offering_types]signature_image_requiredbooleanrequired]{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "name": "string",      "text": "string",      "status": "Active",      "when_required": [        "signup"      ],      "signature_image_required": true    }  ]}SchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [idintegerrequirednamestringrequiredtextstringrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [waiver]statusstringrequiredPossible values: [Active, Archived]when_requiredstring[]requiredPossible values: [signup, all_memberships, all_offering_types]signature_image_requiredbooleanrequired]&lt;root&gt;  &lt;count&gt;123&lt;/count&gt;  &lt;next&gt;http://api.example.org/accounts/?page=4&lt;/next&gt;  &lt;previous&gt;http://api.example.org/accounts/?page=2&lt;/previous&gt;  &lt;results&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;    &lt;text&gt;string&lt;/text&gt;    &lt;status&gt;Active&lt;/status&gt;    &lt;when_required&gt;signup&lt;/when_required&gt;    &lt;signature_image_required&gt;true&lt;/signature_image_required&gt;  &lt;/results&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/waivers", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersapplicable_to — queryall_offering_typesall_membershipsexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlpage — querypage_size — querystatus — query---02TeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousWaiversNextRetrieveCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "name": "string",      "text": "string",      "status": "Active",      "when_required": [        "signup"      ],      "signature_image_required": true    }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


