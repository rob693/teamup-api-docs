# Endpoints_External Calendars Staff Calendar Settings Retrieve

**Method:** GET
**URL:** `/api/v2//external_calendars/staff_calendar_settings/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//external_calendars/staff_calendar_settings/:id
The following condition must be met: is_feature_on
Path Parametersid integerrequiredA unique integer value identifying this provider user reciprocal calendar settings.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [GOOG, MSFT]account_idstringrequiredusernamestringrequired{  "base64_calendar_source_calendar_id": "string",  "calendar_source_calendar_id": "string",  "constrain_only_busy": true,  "id": 0,  "is_active": true,  "is_destination_for_teamup_events": true,  "is_source_for_busy_periods": true,  "calendar_ready": true,  "events_ready": true,  "push_only_if_event_has_attendees": true,  "reminder_number_of_minutes_prior": 0,  "set_external_reminders_for_pushed_events": true,  "calendar_source_account": {    "id": 0,    "calendar_source": "GOOG",    "account_id": "string",    "username": "string"  }}SchemaExample (auto)Schemabase64_calendar_source_calendar_idstringrequiredcalendar_source_calendar_idstringrequiredconstrain_only_busybooleanrequiredIf True, only consider the 'busy events' when checking busy periods.idintegerrequiredis_activebooleanrequiredReturns True if the calendar settings are active.
Possible values: [GOOG, MSFT]account_idstringrequiredusernamestringrequired&lt;root&gt;  &lt;base64_calendar_source_calendar_id&gt;string&lt;/base64_calendar_source_calendar_id&gt;  &lt;calendar_source_calendar_id&gt;string&lt;/calendar_source_calendar_id&gt;  &lt;constrain_only_busy&gt;true&lt;/constrain_only_busy&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;is_active&gt;true&lt;/is_active&gt;  &lt;is_destination_for_teamup_events&gt;true&lt;/is_destination_for_teamup_events&gt;  &lt;is_source_for_busy_periods&gt;true&lt;/is_source_for_busy_periods&gt;  &lt;calendar_ready&gt;true&lt;/calendar_ready&gt;  &lt;events_ready&gt;true&lt;/events_ready&gt;  &lt;push_only_if_event_has_attendees&gt;true&lt;/push_only_if_event_has_attendees&gt;  &lt;reminder_number_of_minutes_prior&gt;0&lt;/reminder_number_of_minutes_prior&gt;  &lt;set_external_reminders_for_pushed_events&gt;true&lt;/set_external_reminders_for_pushed_events&gt;  &lt;calendar_source_account&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;calendar_source&gt;GOOG&lt;/calendar_source&gt;    &lt;account_id&gt;string&lt;/account_id&gt;    &lt;username&gt;string&lt;/username&gt;  &lt;/calendar_source_account&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/external_calendars/staff_calendar_settings/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCreateNextUpdateCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "base64_calendar_source_calendar_id": "string",  "calendar_source_calendar_id": "string",  "constrain_only_busy": true,  "id": 0,  "is_active": true,  "is_destination_for_teamup_events": true,  "is_source_for_busy_periods": true,  "calendar_ready": true,  "events_ready": true,  "push_only_if_event_has_attendees": true,  "reminder_number_of_minutes_prior": 0,  "set_external_reminders_for_pushed_events": true,  "calendar_source_account": {    "id": 0,    "calendar_source": "GOOG",    "account_id": "string",    "username": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


