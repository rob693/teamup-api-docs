# Endpoints_External Calendars Accounts Oauth 2 Initiate Create

**Method:** POST
**URL:** `/api/v2//external_calendars/accounts/oauth2/initiate`

## Summary
URL to authorize use of your Google / Microsoft calendars. | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//external_calendars/accounts/oauth2/initiate
The following condition must be met: is_feature_on
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [GOOG, MSFT]redirect_uristringrequiredRedirect URI for after the OAuth flow is completed (or errors out).Query parameters will be appended to this URI:
'error' - if success is 0,  this will be some error codePossible values: non-emptyBodyrequiredcalendar_sourcestringrequired
Possible values: [GOOG, MSFT]redirect_uristringrequiredRedirect URI for after the OAuth flow is completed (or errors out).Query parameters will be appended to this URI:
'error' - if success is 0,  this will be some error codePossible values: non-emptyBodyrequiredcalendar_sourcestringrequired
Possible values: [GOOG, MSFT]redirect_uristringrequiredRedirect URI for after the OAuth flow is completed (or errors out).Query parameters will be appended to this URI:
'error' - if success is 0,  this will be some error codePossible values: non-empty
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemauristringrequiredtimeout_secondsintegerrequired{  "uri": "string",  "timeout_seconds": 0}SchemaExample (auto)Schemauristringrequiredtimeout_secondsintegerrequired&lt;root&gt;  &lt;uri&gt;string&lt;/uri&gt;  &lt;timeout_seconds&gt;0&lt;/timeout_seconds&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "calendar_source": "GOOG",  "redirect_uri": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/external_calendars/accounts/oauth2/initiate", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
## Example Request / Response JSON
```json
{  "uri": "string",  "timeout_seconds": 0}
```

```json
{  "calendar_source": "GOOG",  "redirect_uri": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"calendar_source": "GOOG",
"redirect_uri": "string"
}
```


