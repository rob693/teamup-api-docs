# Endpoints_Reports Course Session Attendances Grouped Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/course_session_attendances`

## Summary
Grouped Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/course_session_attendances.grouped/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, venue_id, venue.id, venue, venue_name, venue.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, booking_method, is_makeup, status, course_session_start_time, course_session.start_time, course_session, day_of_week, count], &gt;= 1statusstring[]Possible values: [no_show, registered, attended]offering_typesinteger[]venuesinteger[]instructorsstringcustomersinteger[]membershipsinteger[]include_futurebooleanDefault value: falsebooking_methodsstring[]Possible values: [session_dropin, membership, course_dropin]is_makeupbooleansession_starts_at_ltestring&lt;date-time&gt;session_starts_at_gtestring&lt;date-time&gt;session_timeframestringpivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, venue_id, venue.id, venue, venue_name, venue.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, booking_method, is_makeup, status, course_session_start_time, course_session.start_time, course_session, day_of_week, count], &gt;= 1statusstring[]Possible values: [no_show, registered, attended]offering_typesinteger[]venuesinteger[]instructorsstringcustomersinteger[]membershipsinteger[]include_futurebooleanDefault value: falsebooking_methodsstring[]Possible values: [session_dropin, membership, course_dropin]is_makeupbooleansession_starts_at_ltestring&lt;date-time&gt;session_starts_at_gtestring&lt;date-time&gt;session_timeframestringpivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, venue_id, venue.id, venue, venue_name, venue.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, booking_method, is_makeup, status, course_session_start_time, course_session.start_time, course_session, day_of_week, count], &gt;= 1statusstring[]Possible values: [no_show, registered, attended]offering_typesinteger[]venuesinteger[]instructorsstringcustomersinteger[]membershipsinteger[]include_futurebooleanDefault value: falsebooking_methodsstring[]Possible values: [session_dropin, membership, course_dropin]is_makeupbooleansession_starts_at_ltestring&lt;date-time&gt;session_starts_at_gtestring&lt;date-time&gt;session_timeframestringpivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "status": [    "no_show"  ],  "offering_types": [    0  ],  "venues": [    0  ],  "instructors": "string",  "customers": [    0  ],  "memberships": [    0  ],  "include_future": False,  "booking_methods": [    "session_dropin"  ],  "is_makeup": True,  "session_starts_at_lte": "2024-07-29T15:51:28.071Z",  "session_starts_at_gte": "2024-07-29T15:51:28.071Z",  "session_timeframe": "string",  "pivot": "all",  "max_pivot_columns": 4})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/course_session_attendances.grouped/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
## Example Request / Response JSON
```json
{id}
```

```json
{  "job": 0}
```

```json
{id}
```

```json
{  "job": 0}
```

```json
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "status": [    "no_show"  ],  "offering_types": [    0  ],  "venues": [    0  ],  "instructors": "string",  "customers": [    0  ],  "memberships": [    0  ],  "include_future": False,  "booking_methods": [    "session_dropin"  ],  "is_makeup": True,  "session_starts_at_lte": "2024-07-29T15:51:28.071Z",  "session_starts_at_gte": "2024-07-29T15:51:28.071Z",  "session_timeframe": "string",  "pivot": "all",  "max_pivot_columns": 4}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"id_gt": 0,
"sort": [
"string"
],
"format": "csv",
"columns": [
"customer_id"
],
"status": [
"no_show"
],
"offering_types": [
0
],
"venues": [
0
],
"instructors": "string",
"customers": [
0
],
"memberships": [
0
],
"include_future": false,
"booking_methods": [
"session_dropin"
],
"is_makeup": true,
"session_starts_at_lte": "2024-07-29T15:51:28.071Z",
"session_starts_at_gte": "2024-07-29T15:51:28.071Z",
"session_timeframe": "string",
"pivot": "all",
"max_pivot_columns": 4
}
```


