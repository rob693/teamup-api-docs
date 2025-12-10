# Endpoints_Venues Blocked Times Retrieve

**Method:** GET
**URL:** `/api/v2//venues/`

## Summary
Blocked Times | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//venues/:id/blocked_times
Must have one of the following permissions: manage_events.
The following condition must be met: request_method_get
Path Parametersid integerrequiredA unique integer value identifying this venue.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [IU, RRTL, GC]venueintegernullabledatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]created_atstring&lt;date-time&gt;requiredapplicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]instructorintegernullable]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]{  "data": [    {      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }      ],      "created_at": "2024-07-29T15:51:28.071Z",      "applicable_to_availability_schedule_type": "IU",      "venue": 0    },    {      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }      ],      "created_at": "2024-07-29T15:51:28.071Z",      "applicable_to_availability_schedule_type": "IU",      "instructor": 0    }  ],  "applicable_to_availability_schedule_type": "IU"}SchemaExample (auto)Schemadata object[]requiredArray [oneOfVenueBlockedTimeInstructorBlockedTimedatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]created_atstring&lt;date-time&gt;requiredapplicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]venueintegernullabledatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]created_atstring&lt;date-time&gt;requiredapplicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]instructorintegernullable]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]&lt;root&gt;  &lt;data&gt;    &lt;date&gt;2024-07-29&lt;/date&gt;    &lt;blocked_times&gt;      &lt;start&gt;string&lt;/start&gt;      &lt;end&gt;string&lt;/end&gt;    &lt;/blocked_times&gt;    &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;    &lt;applicable_to_availability_schedule_type&gt;IU&lt;/applicable_to_availability_schedule_type&gt;    &lt;venue&gt;0&lt;/venue&gt;  &lt;/data&gt;  &lt;data&gt;    &lt;date&gt;2024-07-29&lt;/date&gt;    &lt;blocked_times&gt;      &lt;start&gt;string&lt;/start&gt;      &lt;end&gt;string&lt;/end&gt;    &lt;/blocked_times&gt;    &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;    &lt;applicable_to_availability_schedule_type&gt;IU&lt;/applicable_to_availability_schedule_type&gt;    &lt;instructor&gt;0&lt;/instructor&gt;  &lt;/data&gt;  &lt;applicable_to_availability_schedule_type&gt;IU&lt;/applicable_to_availability_schedule_type&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/venues/:id/blocked_times", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousPartially UpdateNextBlocked TimesCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "data": [    {      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }
```

```json
{      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


