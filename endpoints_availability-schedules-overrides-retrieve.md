# Endpoints_Availability Schedules Overrides Retrieve

**Method:** GET
**URL:** `/api/v2//availability_schedules/`

## Summary
Overrides | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//availability_schedules/:id/overrides
Must have one of the following permissions: manage_events.
The following condition must be met: object_is_own_schedule
Path Parametersid stringrequiredQuery Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaoverrides object[]requiredArray [datestring&lt;date&gt;requiredavailability object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]]{  "overrides": [    {      "date": "2024-07-29",      "availability": [        {          "start": "string",          "end": "string"        }      ]    }  ]}SchemaExample (auto)Schemaoverrides object[]requiredArray [datestring&lt;date&gt;requiredavailability object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]]&lt;overrides&gt;  &lt;date&gt;2024-07-29&lt;/date&gt;  &lt;availability&gt;    &lt;start&gt;string&lt;/start&gt;    &lt;end&gt;string&lt;/end&gt;  &lt;/availability&gt;&lt;/overrides&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/availability_schedules/:id/overrides", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousDelete Availability Schedule Offering TypeNextUpdate OverridesCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "overrides": [    {      "date": "2024-07-29",      "availability": [        {          "start": "string",          "end": "string"        }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


