# Endpoints_Ai Business Advisor Reports Content Retrieve

**Method:** GET
**URL:** `/api/v2//ai/business_advisor_reports/`

## Summary
Get Content | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//ai/business_advisor_reports/:id/content
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this business advisor report.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [business_advisor_report]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;requiredavailable_atstring&lt;date-time&gt;nullableheadlinestringnullableA brief headline summary of the report.contentstring&lt;uri&gt;required{  "id": 0,  "start_date": "2024-07-29",  "end_date": "2024-07-29",  "available_at": "2024-07-29T15:51:28.071Z",  "headline": "string",  "content": "string"}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [business_advisor_report]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;requiredavailable_atstring&lt;date-time&gt;nullableheadlinestringnullableA brief headline summary of the report.contentstring&lt;uri&gt;required&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;start_date&gt;2024-07-29&lt;/start_date&gt;  &lt;end_date&gt;2024-07-29&lt;/end_date&gt;  &lt;available_at&gt;2024-07-29T15:51:28.071Z&lt;/available_at&gt;  &lt;headline&gt;string&lt;/headline&gt;  &lt;content&gt;string&lt;/content&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/ai/business_advisor_reports/:id/content", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousListNextBusiness ClosuresCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "start_date": "2024-07-29",  "end_date": "2024-07-29",  "available_at": "2024-07-29T15:51:28.071Z",  "headline": "string",  "content": "string"}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


