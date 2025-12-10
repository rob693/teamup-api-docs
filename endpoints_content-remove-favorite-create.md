# Endpoints_Content Remove Favorite Create

**Method:** POST
**URL:** `/api/v2//content/`

## Summary
Remove Favorite | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//content/:id/remove_favorite
Path Parametersid integerrequiredA unique integer value identifying this content.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [content]namestringrequiredPossible values: &lt;= 256 charactersdescriptionstringrequiredcollectionintegerrequiredthumbnail objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64instructors object[] DeferredThis field is DEFERRED.Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [instructor]namestringrequiredpicture_urlstringrequireddescriptionstringrequiredpermissions objectrequiredemail_notificationsbooleanrevenuebooleanattendancesbooleansuper_adminbooleancustomersbooleandiscount_codesbooleanmanage_eventsbooleanstorebooleandeveloperbooleancustomer_paymentsbooleaninstructor_attendancesbooleaninstructor_manage_eventsbooleanposbooleanstaffintegerrequiredavailability_schedules object[] DeferredThis field is DEFERRED.Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [null]namestringPossible values: &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUinstructorintegerrequiredis_defaultstringrequiredhas_availabilitystringrequired]icalendar_links object DeferredThis field is DEFERRED.linkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]required]tags object[] DeferredThis field is DEFERRED.Array [idintegerrequirednamestringrequiredPossible values: &lt;= 32 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767filter integer ExpandablerequiredoneOfExpandableFieldContentFilterintegerThis field is EXPANDABLE.idintegerrequirednamestringPossible values: &lt;= 32 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767tagsundefined[] DeferredThis field is DEFERRED.]is_favorited_by_active_customerboolean DeferredThis field is DEFERRED.{  "id": 0,  "name": "string",  "description": "string",  "collection": 0,  "thumbnail": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  },  "instructors": [    {      "id": 0,      "name": "string",      "picture_url": "string",      "description": "string",      "permissions": {        "email_notifications": true,        "revenue": true,        "attendances": true,        "super_admin": true,        "customers": true,        "discount_codes": true,        "manage_events": true,        "store": true,        "developer": true,        "customer_payments": true,        "instructor_attendances": true,        "instructor_manage_events": true,        "pos": true      },      "staff": 0,      "availability_schedules": [        {          "id": 0,          "name": "string",          "venue": 0,          "default_monday": [            {              "start": "string",              "end": "string"            }          ],          "default_tuesday": [            {              "start": "string",              "end": "string"            }          ],          "default_wednesday": [            {              "start": "string",              "end": "string"            }          ],          "default_thursday": [            {              "start": "string",              "end": "string"            }          ],          "default_friday": [            {              "start": "string",              "end": "string"            }          ],          "default_saturday": [            {              "start": "string",              "end": "string"            }          ],          "default_sunday": [            {              "start": "string",              "end": "string"            }          ],          "schedule_type": "IU",          "instructor": 0,          "is_default": "string",          "has_availability": "string"        }      ],      "icalendar_links": {        "link": "string",        "webcal_url": "string",        "integrations": [          null        ]      }    }  ],  "tags": [    {      "id": 0,      "name": "string",      "order": 0,      "filter": 0    }  ],  "is_favorited_by_active_customer": true}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [content]namestringrequiredPossible values: &lt;= 256 charactersdescriptionstringrequiredcollectionintegerrequiredthumbnail objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64instructors object[] DeferredThis field is DEFERRED.Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [instructor]namestringrequiredpicture_urlstringrequireddescriptionstringrequiredpermissions objectrequiredemail_notificationsbooleanrevenuebooleanattendancesbooleansuper_adminbooleancustomersbooleandiscount_codesbooleanmanage_eventsbooleanstorebooleandeveloperbooleancustomer_paymentsbooleaninstructor_attendancesbooleaninstructor_manage_eventsbooleanposbooleanstaffintegerrequiredavailability_schedules object[] DeferredThis field is DEFERRED.Array [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [null]namestringPossible values: &lt;= 32 charactersvenueintegernullabledefault_monday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_tuesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_wednesday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_thursday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_friday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_saturday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]default_sunday object[]Array [startstring&lt;time&gt;requiredendstring&lt;time&gt;required]schedule_typestring
Possible values: [IU, RRTL, GC]Default value: IUinstructorintegerrequiredis_defaultstringrequiredhas_availabilitystringrequired]icalendar_links object DeferredThis field is DEFERRED.linkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]required]tags object[] DeferredThis field is DEFERRED.Array [idintegerrequirednamestringrequiredPossible values: &lt;= 32 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767filter integer ExpandablerequiredoneOfExpandableFieldContentFilterintegerThis field is EXPANDABLE.idintegerrequirednamestringPossible values: &lt;= 32 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767tagsundefined[] DeferredThis field is DEFERRED.]is_favorited_by_active_customerboolean DeferredThis field is DEFERRED.&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;description&gt;string&lt;/description&gt;  &lt;collection&gt;0&lt;/collection&gt;  &lt;thumbnail&gt;    &lt;id&gt;13314&lt;/id&gt;    &lt;url&gt;string&lt;/url&gt;    &lt;original_width&gt;64&lt;/original_width&gt;    &lt;original_height&gt;64&lt;/original_height&gt;  &lt;/thumbnail&gt;  &lt;instructors&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;    &lt;picture_url&gt;string&lt;/picture_url&gt;    &lt;description&gt;string&lt;/description&gt;    &lt;permissions&gt;      &lt;email_notifications&gt;true&lt;/email_notifications&gt;      &lt;revenue&gt;true&lt;/revenue&gt;      &lt;attendances&gt;true&lt;/attendances&gt;      &lt;super_admin&gt;true&lt;/super_admin&gt;      &lt;customers&gt;true&lt;/customers&gt;      &lt;discount_codes&gt;true&lt;/discount_codes&gt;      &lt;manage_events&gt;true&lt;/manage_events&gt;      &lt;store&gt;true&lt;/store&gt;      &lt;developer&gt;true&lt;/developer&gt;      &lt;customer_payments&gt;true&lt;/customer_payments&gt;      &lt;instructor_attendances&gt;true&lt;/instructor_attendances&gt;      &lt;instructor_manage_events&gt;true&lt;/instructor_manage_events&gt;      &lt;pos&gt;true&lt;/pos&gt;    &lt;/permissions&gt;    &lt;staff&gt;0&lt;/staff&gt;    &lt;availability_schedules&gt;      &lt;id&gt;0&lt;/id&gt;      &lt;name&gt;string&lt;/name&gt;      &lt;venue&gt;0&lt;/venue&gt;      &lt;default_monday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_monday&gt;      &lt;default_tuesday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_tuesday&gt;      &lt;default_wednesday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_wednesday&gt;      &lt;default_thursday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_thursday&gt;      &lt;default_friday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_friday&gt;      &lt;default_saturday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_saturday&gt;      &lt;default_sunday&gt;        &lt;start&gt;string&lt;/start&gt;        &lt;end&gt;string&lt;/end&gt;      &lt;/default_sunday&gt;      &lt;schedule_type&gt;IU&lt;/schedule_type&gt;      &lt;instructor&gt;0&lt;/instructor&gt;      &lt;is_default&gt;string&lt;/is_default&gt;      &lt;has_availability&gt;string&lt;/has_availability&gt;    &lt;/availability_schedules&gt;    &lt;icalendar_links&gt;      &lt;link&gt;string&lt;/link&gt;      &lt;webcal_url&gt;string&lt;/webcal_url&gt;      &lt;integrations/&gt;    &lt;/icalendar_links&gt;  &lt;/instructors&gt;  &lt;tags&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;    &lt;order&gt;0&lt;/order&gt;    &lt;filter&gt;0&lt;/filter&gt;  &lt;/tags&gt;  &lt;is_favorited_by_active_customer&gt;true&lt;/is_favorited_by_active_customer&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customer": 0})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/content/:id/remove_favorite", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customer": 0
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "description": "string",  "collection": 0,  "thumbnail": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }
```

```json
{      "id": 0,      "name": "string",      "picture_url": "string",      "description": "string",      "permissions": {        "email_notifications": true,        "revenue": true,        "attendances": true,        "super_admin": true,        "customers": true,        "discount_codes": true,        "manage_events": true,        "store": true,        "developer": true,        "customer_payments": true,        "instructor_attendances": true,        "instructor_manage_events": true,        "pos": true      }
```

```json
{          "id": 0,          "name": "string",          "venue": 0,          "default_monday": [            {              "start": "string",              "end": "string"            }
```

```json
{              "start": "string",              "end": "string"            }
```

```json
{              "start": "string",              "end": "string"            }
```

```json
{              "start": "string",              "end": "string"            }
```

```json
{              "start": "string",              "end": "string"            }
```

```json
{              "start": "string",              "end": "string"            }
```

```json
{              "start": "string",              "end": "string"            }
```

```json
{        "link": "string",        "webcal_url": "string",        "integrations": [          null        ]      }
```

```json
{      "id": 0,      "name": "string",      "order": 0,      "filter": 0    }
```

```json
{  "customer": 0}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"customer": 0
}
```


