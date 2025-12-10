# Endpoints_Availability Schedules Offering Types Destroy

**Method:** DELETE
**URL:** `/api/v2//availability_schedules/`

## Summary
Delete Availability Schedule Offering Type | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

DELETE https://goteamup.com/api/v2//availability_schedules/:id/offering_types/:offering_type_id
Must have one of the following permissions: manage_events.
The following condition must be met: object_is_own_schedule
Path Parametersid stringrequiredoffering_type_id stringrequiredPossible values: Value must match regular expression ^\d+$Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaoneOfRoomRentalAvailabilityScheduleInstructorAvailabilityScheduleidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [null]namestringPossible values: &lt;= 32 charactersvenue integer ExpandableoneOfExpandableFieldVenueReadintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [venue]namestringrequiredPossible values: &lt;= 200 charactersdescriptionstringnullableaddressstringrequiredphysical_address objectnullablestreetstringrequiredstreet_secondarystringnullablerequiredcitystringrequiredregionstringrequiredpostal_codestringrequiredcountrystringrequiredlatnumber&lt;double&gt;lngnumber&lt;double&gt;timezonestringrequiredPossible values: &lt;= 250 charactersvideo_urlstringnullablezoom_userintegerrequiredvenue_typestringrequiredPossible values: [physical, online]venue_rooms string ExpandablerequiredoneOfExpandableFieldVenueRoom[]stringA URL to a collection of related resources. This field is EXPANDABLE.Example: https://goteamup.com/api/v2/related_collectionArray [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [venue_room]statusstringrequiredPossible values: [active, archived]namestringrequiredPossible values: &lt;= 64 charactersvenue integer ExpandablerequiredoneOfExpandableField1-item-propertiesintegerThis field is EXPANDABLE.thumbnail objectidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [image]urlstring&lt;uri&gt;requiredprofileintegernullableoriginal_widthintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647original_heightintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647userintegernullablecreated_atstring&lt;date-time&gt;required]latnumber&lt;double&gt;requiredlngnumber&lt;double&gt;requiredarchivedbooleanrequiredis_onlinebooleanrequiredvideo_url_typestringPossible values: [static, zoom]default_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUoffering_types object[] DeferredThis field is DEFERRED.Array [allows_dropinsbooleanrequiredappointment_settings object ExpandablerequiredoneOfExpandableFieldobjectdurationintegerrequiredThe duration in minutes.Possible values: &gt;= 5 and &lt;= 1440buffer_beforeintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0buffer_afterintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0start_time_incrementsnullable
Possible values: [null, 15, 30, 45, 60]default_venueintegerrequireddefault_venue_roomsinteger[]requireddurationintegerrequiredThe duration in minutes.Possible values: &gt;= 5 and &lt;= 1440buffer_beforeintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0buffer_afterintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0start_time_incrementsnullable
Possible values: [null, 15, 30, 45, 60]default_venueintegerrequireddefault_venue_roomsinteger[]requiredbackground_colorstringrequiredcancellation_notice_intervalintegerThe duration in minutes.Default value: 0category integer ExpandablerequiredoneOfExpandableFieldOfferingTypeCategoryReadintegernullableThis field is EXPANDABLE.idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [offering_type_category]nameCategory Name (string)requiredPossible values: &lt;= 256 charactersimage objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64colorstringrequiredcustomer_visibilitystringrequiredPossible values: [public, membership_holders, private]descriptionstringnullabledropin_pricestringrequiredhas_active_schedulesbooleanrequiredhas_pricingbooleanrequiredidintegerrequiredimage objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64instructors string ExpandablerequiredoneOfExpandableFieldInstructor[]stringA URL to a collection of related resources. This field is EXPANDABLE.Example: https://goteamup.com/api/v2/related_collectionArray [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [instructor]namestringrequiredpicture_urlstringrequireddescriptionstringrequiredpermissions objectrequiredemail_notificationsbooleanrevenuebooleanattendancesbooleansuper_adminbooleancustomersbooleandiscount_codesbooleanmanage_eventsbooleanstorebooleandeveloperbooleancustomer_paymentsbooleaninstructor_attendancesbooleaninstructor_manage_eventsbooleanposbooleanstaffintegerrequiredavailability_schedules object[] DeferredThis field is DEFERRED.Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [null]namestringPossible values: &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUinstructorintegerrequiredis_defaultstringrequiredhas_availabilitystringrequired]icalendar_links object DeferredThis field is DEFERRED.linkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]required]is_draftbooleanrequiredmax_allowed_ageintegernullableCan be no older than this many years to registerPossible values: &gt;= -2147483648 and &lt;= 2147483647memberships_countintegerrequiredmemberships_summary_descriptionstringrequiredmin_allowed_ageintegernullableMust be at least this many years old to registerPossible values: &gt;= -2147483648 and &lt;= 2147483647namestringrequiredPossible values: &lt;= 256 charactersobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [offering_type]orderintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647registrations_close_intervalintegerThe duration in minutes.Default value: 0registrations_open_intervalintegerThe duration in minutes.Default value: 0room_rental_settings object ExpandablerequiredoneOfExpandableFieldobjectdurationintegerrequiredThe duration in minutes.Possible values: &gt;= 5 and &lt;= 1440buffer_beforeintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0buffer_afterintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0start_time_incrementsnullable
Possible values: [null, 15, 30, 45, 60]room_uniformitybooleanrequireddurationintegerrequiredThe duration in minutes.Possible values: &gt;= 5 and &lt;= 1440buffer_beforeintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0buffer_afterintegerThe duration in minutes.Possible values: &gt;= 0 and &lt;= 1440Default value: 0start_time_incrementsnullable
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
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


