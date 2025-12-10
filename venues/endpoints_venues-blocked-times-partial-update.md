# Endpoints_Venues Blocked Times Partial Update

**Method:** PATCH
**URL:** `/api/v2//venues/`

## Summary
Blocked Times | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//venues/:id/blocked_times
Must have one of the following permissions: manage_events.
The following condition must be met: request_method_get
Path Parametersid integerrequiredA unique integer value identifying this venue.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [IU, RRTL, GC]venueintegernullabledatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]instructorintegernullable]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]Bodydata object[]Array [oneOfVenueBlockedTimeInstructorBlockedTimedatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]venueintegernullabledatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]instructorintegernullable]applicable_to_availability_schedule_typestring
Possible values: [IU, RRTL, GC]Bodydata object[]Array [oneOfVenueBlockedTimeInstructorBlockedTimedatestring&lt;date&gt;requiredblocked_times object[]requiredArray [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]applicable_to_availability_schedule_typestring
## Example Request / Response JSON
```json
{  "data": [    {      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }
```

```json
{      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }
```

```json
{  "data": [    {      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }
```

```json
{      "date": "2024-07-29",      "blocked_times": [        {          "start": "string",          "end": "string"        }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"data": [
{
"date": "2024-07-29",
"blocked_times": [
{
"start": "string",
"end": "string"
}
```

```json
{
"date": "2024-07-29",
"blocked_times": [
{
"start": "string",
"end": "string"
}
```


