# Endpoints_Events Registration Timelines Resolved Retrieve

**Method:** GET
**URL:** `/api/v2//events/`

## Summary
Resolved Registration Timelines | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//events/:id/registration_timelines/resolved
Must have one of the following permissions: manage_events, attendances, instructor_manage_events, instructor_attendances, developer, pos.
Path Parametersid integerrequiredA unique integer value identifying this event.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaregistration_timeline objectrequiredidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [registration_timeline]namestringnullablePossible values: &lt;= 256 charactersaudience_typestringrequiredPossible values: [everyone, business_only, membership_holders, specific_memberships, specific_customers, private_url]thumbnail objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64calendar_opens_atstringrequiredregistrations_open_atstringrequiredregistrations_close_atstringrequiredlate_cancels_afterstringrequired{  "registration_timeline": {    "id": 0,    "name": "string",    "audience_type": "everyone",    "thumbnail": {      "id": 13314,      "url": "string",      "original_width": 64,      "original_height": 64    }  },  "calendar_opens_at": "string",  "registrations_open_at": "string",  "registrations_close_at": "string",  "late_cancels_after": "string"}SchemaExample (auto)Schemaregistration_timeline objectrequiredidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [registration_timeline]namestringnullablePossible values: &lt;= 256 charactersaudience_typestringrequiredPossible values: [everyone, business_only, membership_holders, specific_memberships, specific_customers, private_url]thumbnail objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64calendar_opens_atstringrequiredregistrations_open_atstringrequiredregistrations_close_atstringrequiredlate_cancels_afterstringrequired&lt;root&gt;  &lt;registration_timeline&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;    &lt;audience_type&gt;everyone&lt;/audience_type&gt;    &lt;thumbnail&gt;      &lt;id&gt;13314&lt;/id&gt;      &lt;url&gt;string&lt;/url&gt;      &lt;original_width&gt;64&lt;/original_width&gt;      &lt;original_height&gt;64&lt;/original_height&gt;    &lt;/thumbnail&gt;  &lt;/registration_timeline&gt;  &lt;calendar_opens_at&gt;string&lt;/calendar_opens_at&gt;  &lt;registrations_open_at&gt;string&lt;/registrations_open_at&gt;  &lt;registrations_close_at&gt;string&lt;/registrations_close_at&gt;  &lt;late_cancels_after&gt;string&lt;/late_cancels_after&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/events/:id/registration_timelines/resolved", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousRegisterNextUnregisterCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "registration_timeline": {    "id": 0,    "name": "string",    "audience_type": "everyone",    "thumbnail": {      "id": 13314,      "url": "string",      "original_width": 64,      "original_height": 64    }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


