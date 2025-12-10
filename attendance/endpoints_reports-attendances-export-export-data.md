# Endpoints_Reports Attendances Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/attendances/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/attendances/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, event_id, event.id, event, event_starts_at, event.starts_at, event_ends_at, event.ends_at, event_name, event.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, booking_source, status, checkin_ocurred_at, checkin.ocurred_at, checkin, is_first_attendance]customersinteger[]customer_membershipsinteger[]membershipsinteger[]statusstring[]Possible values: [attended, registered, no_show, late_cancelled]attendance_statusstring[]Possible values: [attended, registered, no_show, late_cancelled]booking_methodsstring[]Possible values: [membership, dropin, free]booking_sourcesstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$event_typesstring[]Possible values: [appointment, class]include_futurebooleanDefault value: falseinstructorsstringoffering_typesinteger[]venuesinteger[]updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;event_start_ltestring&lt;date-time&gt;event_start_gtestring&lt;date-time&gt;event_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, event_id, event.id, event, event_starts_at, event.starts_at, event_ends_at, event.ends_at, event_name, event.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, booking_source, status, checkin_ocurred_at, checkin.ocurred_at, checkin, is_first_attendance]customersinteger[]customer_membershipsinteger[]membershipsinteger[]statusstring[]Possible values: [attended, registered, no_show, late_cancelled]attendance_statusstring[]Possible values: [attended, registered, no_show, late_cancelled]booking_methodsstring[]Possible values: [membership, dropin, free]booking_sourcesstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$event_typesstring[]Possible values: [appointment, class]include_futurebooleanDefault value: falseinstructorsstringoffering_typesinteger[]venuesinteger[]updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;event_start_ltestring&lt;date-time&gt;event_start_gtestring&lt;date-time&gt;event_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, event_id, event.id, event, event_starts_at, event.starts_at, event_ends_at, event.ends_at, event_name, event.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, booking_source, status, checkin_ocurred_at, checkin.ocurred_at, checkin, is_first_attendance]customersinteger[]customer_membershipsinteger[]membershipsinteger[]statusstring[]Possible values: [attended, registered, no_show, late_cancelled]attendance_statusstring[]Possible values: [attended, registered, no_show, late_cancelled]booking_methodsstring[]Possible values: [membership, dropin, free]booking_sourcesstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$event_typesstring[]Possible values: [appointment, class]include_futurebooleanDefault value: falseinstructorsstringoffering_typesinteger[]venuesinteger[]updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;event_start_ltestring&lt;date-time&gt;event_start_gtestring&lt;date-time&gt;event_timeframestring
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "customers": [    0  ],  "customer_memberships": [    0  ],  "memberships": [    0  ],  "status": [    "attended"  ],  "attendance_status": [    "attended"  ],  "booking_methods": [    "membership"  ],  "booking_sources": [    "string"  ],  "event_types": [    "appointment"  ],  "include_future": False,  "instructors": "string",  "offering_types": [    0  ],  "venues": [    0  ],  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "event_start_lte": "2024-07-29T15:51:28.071Z",  "event_start_gte": "2024-07-29T15:51:28.071Z",  "event_timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/attendances/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "customers": [    0  ],  "customer_memberships": [    0  ],  "memberships": [    0  ],  "status": [    "attended"  ],  "attendance_status": [    "attended"  ],  "booking_methods": [    "membership"  ],  "booking_sources": [    "string"  ],  "event_types": [    "appointment"  ],  "include_future": False,  "instructors": "string",  "offering_types": [    0  ],  "venues": [    0  ],  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "event_start_lte": "2024-07-29T15:51:28.071Z",  "event_start_gte": "2024-07-29T15:51:28.071Z",  "event_timeframe": "string"}
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
"customers": [
0
],
"customer_memberships": [
0
],
"memberships": [
0
],
"status": [
"attended"
],
"attendance_status": [
"attended"
],
"booking_methods": [
"membership"
],
"booking_sources": [
"string"
],
"event_types": [
"appointment"
],
"include_future": false,
"instructors": "string",
"offering_types": [
0
],
"venues": [
0
],
"updated_at_lte": "2024-07-29T15:51:28.071Z",
"updated_at_gte": "2024-07-29T15:51:28.071Z",
"event_start_lte": "2024-07-29T15:51:28.071Z",
"event_start_gte": "2024-07-29T15:51:28.071Z",
"event_timeframe": "string"
}
```


