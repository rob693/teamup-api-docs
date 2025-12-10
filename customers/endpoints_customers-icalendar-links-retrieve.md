# Endpoints_Customers Icalendar Links Retrieve

**Method:** GET
**URL:** `/api/v2//customers/`

## Summary
Icalendar Links | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customers/:id/icalendar_links
Path Parametersid integerrequiredA unique integer value identifying this provider customer profile.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemalinkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]required{  "link": "string",  "webcal_url": "string",  "integrations": [    null  ]}SchemaExample (auto)Schemalinkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]required&lt;root&gt;  &lt;link&gt;string&lt;/link&gt;  &lt;webcal_url&gt;string&lt;/webcal_url&gt;  &lt;integrations/&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customers/:id/icalendar_links", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousChange PasswordNextNotification PreferencesCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "link": "string",  "webcal_url": "string",  "integrations": [    null  ]}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


