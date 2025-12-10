# Endpoints_Reports Instructed Sessions Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/instructed_sessions/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/instructed_sessions/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, instructor_thumbnail_url, instructor.thumbnail_url, starts_at, venue_id, venue.id, venue, venue_name, venue.name, venue_timezone, max_occupancy, hours, attended_count, no_show_count, late_cancel_count, attended_comped_count, comped_counts.attended, comped_counts, session_type, instructor_pay_rate_id, instructor_pay_rate.id, instructor_pay_rate, instructor_pay_rate_name, instructor_pay_rate.name, instructor_pay_rate_type, instructor_pay_rate.type, instructor_pay_rate_base, instructor_pay_rate.base, instructor_pay, pay_rate_tiers, instructor_pay_rate.tiers, instructor_pay_calculation_pending]instructorsstringsession_typesstring[]Possible values: [class, course_session]pay_ratesinteger[]offering_typesinteger[]venuesinteger[]starts_at_gtestring&lt;date-time&gt;starts_at_ltestring&lt;date-time&gt;timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, instructor_thumbnail_url, instructor.thumbnail_url, starts_at, venue_id, venue.id, venue, venue_name, venue.name, venue_timezone, max_occupancy, hours, attended_count, no_show_count, late_cancel_count, attended_comped_count, comped_counts.attended, comped_counts, session_type, instructor_pay_rate_id, instructor_pay_rate.id, instructor_pay_rate, instructor_pay_rate_name, instructor_pay_rate.name, instructor_pay_rate_type, instructor_pay_rate.type, instructor_pay_rate_base, instructor_pay_rate.base, instructor_pay, pay_rate_tiers, instructor_pay_rate.tiers, instructor_pay_calculation_pending]instructorsstringsession_typesstring[]Possible values: [class, course_session]pay_ratesinteger[]offering_typesinteger[]venuesinteger[]starts_at_gtestring&lt;date-time&gt;starts_at_ltestring&lt;date-time&gt;timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, instructor_thumbnail_url, instructor.thumbnail_url, starts_at, venue_id, venue.id, venue, venue_name, venue.name, venue_timezone, max_occupancy, hours, attended_count, no_show_count, late_cancel_count, attended_comped_count, comped_counts.attended, comped_counts, session_type, instructor_pay_rate_id, instructor_pay_rate.id, instructor_pay_rate, instructor_pay_rate_name, instructor_pay_rate.name, instructor_pay_rate_type, instructor_pay_rate.type, instructor_pay_rate_base, instructor_pay_rate.base, instructor_pay, pay_rate_tiers, instructor_pay_rate.tiers, instructor_pay_calculation_pending]instructorsstringsession_typesstring[]Possible values: [class, course_session]pay_ratesinteger[]offering_typesinteger[]venuesinteger[]starts_at_gtestring&lt;date-time&gt;starts_at_ltestring&lt;date-time&gt;timeframestring
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "instructors": "string",  "session_types": [    "class"  ],  "pay_rates": [    0  ],  "offering_types": [    0  ],  "venues": [    0  ],  "starts_at_gte": "2024-07-29T15:51:28.071Z",  "starts_at_lte": "2024-07-29T15:51:28.071Z",  "timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/instructed_sessions/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"id_gt": 0,
"sort": [
"format": "csv",
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "instructors": "string",  "session_types": [    "class"  ],  "pay_rates": [    0  ],  "offering_types": [    0  ],  "venues": [    0  ],  "starts_at_gte": "2024-07-29T15:51:28.071Z",  "starts_at_lte": "2024-07-29T15:51:28.071Z",  "timeframe": "string"}
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
"id"
],
"instructors": "string",
"session_types": [
"class"
],
"pay_rates": [
0
],
"offering_types": [
0
],
"venues": [
0
],
"starts_at_gte": "2024-07-29T15:51:28.071Z",
"starts_at_lte": "2024-07-29T15:51:28.071Z",
"timeframe": "string"
}
```


