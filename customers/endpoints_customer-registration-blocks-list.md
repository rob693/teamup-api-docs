# Endpoints_Customer Registration Blocks List

**Method:** GET
**URL:** `/api/v2//customer_registration_blocks`

## Summary
List | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customer_registration_blocks
Query Parameterscustomer integer[]expand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]is_active booleanpage integerA page number within the paginated result set.page_size integerPossible values: &lt;= 100Number of results to return per page.Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [idintegerrequiredcustomerintegerrequiredis_activebooleanrequiredcreated_atstring&lt;date-time&gt;deactivated_atstring&lt;date-time&gt;nullable]{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "customer": 0,      "is_active": true,      "created_at": "2024-07-29T15:51:28.071Z",      "deactivated_at": "2024-07-29T15:51:28.071Z"    }  ]}SchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [idintegerrequiredcustomerintegerrequiredis_activebooleanrequiredcreated_atstring&lt;date-time&gt;deactivated_atstring&lt;date-time&gt;nullable]&lt;root&gt;  &lt;count&gt;123&lt;/count&gt;  &lt;next&gt;http://api.example.org/accounts/?page=4&lt;/next&gt;  &lt;previous&gt;http://api.example.org/accounts/?page=2&lt;/previous&gt;  &lt;results&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;customer&gt;0&lt;/customer&gt;    &lt;is_active&gt;true&lt;/is_active&gt;    &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;    &lt;deactivated_at&gt;2024-07-29T15:51:28.071Z&lt;/deactivated_at&gt;  &lt;/results&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customer_registration_blocks", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscustomer — queryAdd itemexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlis_active — query---truefalsepage — querypage_size — queryTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCustomer Registration BlocksNextRetrieveCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "customer": 0,      "is_active": true,      "created_at": "2024-07-29T15:51:28.071Z",      "deactivated_at": "2024-07-29T15:51:28.071Z"    }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


