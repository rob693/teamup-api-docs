# Endpoints_Availability Schedules Update

**Method:** PUT
**URL:** `/api/v2//availability_schedules/`

## Summary
Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//availability_schedules/:id
Must have one of the following permissions: manage_events.
The following condition must be met: object_is_own_schedule
Path Parametersid stringrequiredQuery Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyoneOfRoomRentalAvailabilityScheduleInstructorAvailabilitySchedulenamestringPossible values: non-empty and &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUnamestringPossible values: non-empty and &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUinstructorintegerrequiredBodyoneOfRoomRentalAvailabilityScheduleInstructorAvailabilitySchedulenamestringPossible values: non-empty and &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUnamestringPossible values: non-empty and &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUinstructorintegerrequiredBodyoneOfRoomRentalAvailabilityScheduleInstructorAvailabilitySchedulenamestringPossible values: non-empty and &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUnamestringPossible values: non-empty and &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "venue": 0,  "default_monday": [    {      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "allows_dropins": true,      "appointment_settings": {        "duration": 0,        "buffer_before": 0,        "buffer_after": 0,        "default_venue": 0,        "default_venue_rooms": [          0        ]      }
```

```json
{        "id": 13314,        "url": "string",        "original_width": 64,        "original_height": 64      }
```

```json
{        "duration": 0,        "buffer_before": 0,        "buffer_after": 0,        "room_uniformity": true      }
```

```json
{          "offering_type": 0,          "availability_schedule": 0,          "venue_rooms": [            0          ]        }
```

```json
{          "id": 0,          "type": "pack",          "name": "string",          "description": "string",          "begin_on_first_registration": true,          "start_date": "2024-07-29",          "expiration_date": "2024-07-29",          "duration": 0,          "duration_unit": "days",          "one_time_fee": {            "decimal": 0,            "string": "£45",            "iso_currency_code": "gbp",            "currency_symbol": "£",            "currency_symbol_position": "before"          }
```

```json
{            "decimal": 0,            "string": "£45",            "iso_currency_code": "gbp",            "currency_symbol": "£",            "currency_symbol_position": "before"          }
```

```json
{            "decimal": 0,            "string": "£45",            "iso_currency_code": "gbp",            "currency_symbol": "£",            "currency_symbol_position": "before"          }
```

```json
{          "id": 0,          "name": "string",          "audience_type": "everyone",          "thumbnail": {            "id": 13314,            "url": "string",            "original_width": 64,            "original_height": 64          }
```

```json
{      "offering_type": 0,      "availability_schedule": 0,      "venue_rooms": [        0      ]    }
```

```json
{  "name": "string",  "venue": 0,  "default_monday": [    {      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{      "start": "string",      "end": "string"    }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"venue": 0,
"default_monday": [
{
"start": "string",
"end": "string"
}
```

```json
{
"start": "string",
"end": "string"
}
```

```json
{
"start": "string",
"end": "string"
}
```

```json
{
"start": "string",
"end": "string"
}
```

```json
{
"start": "string",
"end": "string"
}
```

```json
{
"start": "string",
"end": "string"
}
```

```json
{
"start": "string",
"end": "string"
}
```


