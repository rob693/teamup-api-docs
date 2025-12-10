# Endpoints_External Calendars Accounts Calendars Retrieve 2

**Method:** GET
**URL:** `/api/v2//external_calendars/accounts/`

## Summary
Retrieve a specific calendar. | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//external_calendars/accounts/:id/calendars/:base64_calendar_id
The following condition must be met: is_feature_on
Path Parametersbase64_calendar_id stringrequiredid integerrequiredA unique integer value identifying this Calendar Source Account.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [GOOG, MSFT]account_idstringrequiredusernamestringrequired{  "id": 0,  "calendar_source": "GOOG",  "account_id": "string",  "username": "string"}SchemaExample (auto)Schemaidintegerrequiredcalendar_sourcestringrequired
Possible values: [GOOG, MSFT]account_idstringrequiredusernamestringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;calendar_source&gt;GOOG&lt;/calendar_source&gt;  &lt;account_id&gt;string&lt;/account_id&gt;  &lt;username&gt;string&lt;/username&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/external_calendars/accounts/:id/calendars/:base64_calendar_id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersbase64_calendar_id — pathrequiredid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousList all calendars.NextURL to authorize use of your Google / Microsoft calendars.CompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "calendar_source": "GOOG",  "account_id": "string",  "username": "string"}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


