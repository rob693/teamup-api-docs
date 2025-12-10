# Endpoints_Reports Course Session Attendances Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/course_session_attendances/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/course_session_attendances/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, course_session_id, course_session.id, course_session, course_session_starts_at, course_session.starts_at, course_id, course.id, course, course_name, course.name, course_series_id, course_series.id, course_series, course_series_name, course_series.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, is_makeup, status]statusstring[]Possible values: [no_show, registered, attended]offering_typesinteger[]venuesinteger[]instructorsstringcustomersinteger[]membershipsinteger[]include_futurebooleanDefault value: falsebooking_methodsstring[]Possible values: [session_dropin, membership, course_dropin]is_makeupbooleansession_starts_at_ltestring&lt;date-time&gt;session_starts_at_gtestring&lt;date-time&gt;session_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, course_session_id, course_session.id, course_session, course_session_starts_at, course_session.starts_at, course_id, course.id, course, course_name, course.name, course_series_id, course_series.id, course_series, course_series_name, course_series.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, is_makeup, status]statusstring[]Possible values: [no_show, registered, attended]offering_typesinteger[]venuesinteger[]instructorsstringcustomersinteger[]membershipsinteger[]include_futurebooleanDefault value: falsebooking_methodsstring[]Possible values: [session_dropin, membership, course_dropin]is_makeupbooleansession_starts_at_ltestring&lt;date-time&gt;session_starts_at_gtestring&lt;date-time&gt;session_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, course_session_id, course_session.id, course_session, course_session_starts_at, course_session.starts_at, course_id, course.id, course, course_name, course.name, course_series_id, course_series.id, course_series, course_series_name, course_series.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, is_makeup, status]statusstring[]Possible values: [no_show, registered, attended]offering_typesinteger[]venuesinteger[]instructorsstringcustomersinteger[]membershipsinteger[]include_futurebooleanDefault value: falsebooking_methodsstring[]Possible values: [session_dropin, membership, course_dropin]is_makeupbooleansession_starts_at_ltestring&lt;date-time&gt;session_starts_at_gtestring&lt;date-time&gt;session_timeframestring
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "status": [    "no_show"  ],  "offering_types": [    0  ],  "venues": [    0  ],  "instructors": "string",  "customers": [    0  ],  "memberships": [    0  ],  "include_future": False,  "booking_methods": [    "session_dropin"  ],  "is_makeup": True,  "session_starts_at_lte": "2024-07-29T15:51:28.071Z",  "session_starts_at_gte": "2024-07-29T15:51:28.071Z",  "session_timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/course_session_attendances/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "status": [    "no_show"  ],  "offering_types": [    0  ],  "venues": [    0  ],  "instructors": "string",  "customers": [    0  ],  "memberships": [    0  ],  "include_future": False,  "booking_methods": [    "session_dropin"  ],  "is_makeup": True,  "session_starts_at_lte": "2024-07-29T15:51:28.071Z",  "session_starts_at_gte": "2024-07-29T15:51:28.071Z",  "session_timeframe": "string"}
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
"session_timeframe": "string"
}
```


