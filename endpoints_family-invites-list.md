# Endpoints_Family Invites List

**Method:** GET
**URL:** `/api/v2//family_invites`

## Summary
List | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//family_invites
Query Parametersclaimed booleanexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]page integerA page number within the paginated result set.page_size integerPossible values: &lt;= 100Number of results to return per page.Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [family_invite]first_namestringrequiredPossible values: &lt;= 256 characterslast_namestringrequiredPossible values: &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: &lt;= 254 charactersclaim_urlstringrequiredclaimed_byintegernullable]{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "first_name": "string",      "last_name": "string",      "email": "user@example.com",      "claim_url": "string",      "claimed_by": 0    }  ]}SchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [family_invite]first_namestringrequiredPossible values: &lt;= 256 characterslast_namestringrequiredPossible values: &lt;= 256 charactersemailstring&lt;email&gt;requiredPossible values: &lt;= 254 charactersclaim_urlstringrequiredclaimed_byintegernullable]&lt;root&gt;  &lt;count&gt;123&lt;/count&gt;  &lt;next&gt;http://api.example.org/accounts/?page=4&lt;/next&gt;  &lt;previous&gt;http://api.example.org/accounts/?page=2&lt;/previous&gt;  &lt;results&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;first_name&gt;string&lt;/first_name&gt;    &lt;last_name&gt;string&lt;/last_name&gt;    &lt;email&gt;user@example.com&lt;/email&gt;    &lt;claim_url&gt;string&lt;/claim_url&gt;    &lt;claimed_by&gt;0&lt;/claimed_by&gt;  &lt;/results&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/family_invites", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersclaimed — query---truefalseexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlpage — querypage_size — queryTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousFamily InvitesNextCreateCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "first_name": "string",      "last_name": "string",      "email": "user@example.com",      "claim_url": "string",      "claimed_by": 0    }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


