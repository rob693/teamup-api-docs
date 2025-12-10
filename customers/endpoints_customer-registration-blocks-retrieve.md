# Endpoints_Customer Registration Blocks Retrieve

**Method:** GET
**URL:** `/api/v2//customer_registration_blocks/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customer_registration_blocks/:id
Path Parametersid integerrequiredA unique integer value identifying this customer registration block.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaidintegerrequiredcustomerintegerrequiredis_activebooleanrequiredcreated_atstring&lt;date-time&gt;deactivated_atstring&lt;date-time&gt;nullable{  "id": 0,  "customer": 0,  "is_active": true,  "created_at": "2024-07-29T15:51:28.071Z",  "deactivated_at": "2024-07-29T15:51:28.071Z"}SchemaExample (auto)Schemaidintegerrequiredcustomerintegerrequiredis_activebooleanrequiredcreated_atstring&lt;date-time&gt;deactivated_atstring&lt;date-time&gt;nullable&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;customer&gt;0&lt;/customer&gt;  &lt;is_active&gt;true&lt;/is_active&gt;  &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;  &lt;deactivated_at&gt;2024-07-29T15:51:28.071Z&lt;/deactivated_at&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customer_registration_blocks/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousListNextCustomersCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "customer": 0,  "is_active": true,  "created_at": "2024-07-29T15:51:28.071Z",  "deactivated_at": "2024-07-29T15:51:28.071Z"}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


