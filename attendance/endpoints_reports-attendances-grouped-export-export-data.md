# Endpoints_Reports Attendances Grouped Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/attendances`

## Summary
Grouped Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/attendances.grouped/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, day_of_week, event_start_time, event.start_time, event, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, booking_method, booking_source, status, count], &gt;= 1customersinteger[]customer_membershipsinteger[]membershipsinteger[]statusstring[]Possible values: [attended, registered, no_show, late_cancelled]attendance_statusstring[]Possible values: [attended, registered, no_show, late_cancelled]booking_methodsstring[]Possible values: [membership, dropin, free]booking_sourcesstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$event_typesstring[]Possible values: [appointment, class]include_futurebooleanDefault value: falseinstructorsstringoffering_typesinteger[]venuesinteger[]updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;event_start_ltestring&lt;date-time&gt;event_start_gtestring&lt;date-time&gt;event_timeframestringpivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, day_of_week, event_start_time, event.start_time, event, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, booking_method, booking_source, status, count], &gt;= 1customersinteger[]customer_membershipsinteger[]membershipsinteger[]statusstring[]Possible values: [attended, registered, no_show, late_cancelled]attendance_statusstring[]Possible values: [attended, registered, no_show, late_cancelled]booking_methodsstring[]Possible values: [membership, dropin, free]booking_sourcesstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$event_typesstring[]Possible values: [appointment, class]include_futurebooleanDefault value: falseinstructorsstringoffering_typesinteger[]venuesinteger[]updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;event_start_ltestring&lt;date-time&gt;event_start_gtestring&lt;date-time&gt;event_timeframestringpivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, day_of_week, event_start_time, event.start_time, event, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, booking_method, booking_source, status, count], &gt;= 1customersinteger[]customer_membershipsinteger[]membershipsinteger[]statusstring[]Possible values: [attended, registered, no_show, late_cancelled]attendance_statusstring[]Possible values: [attended, registered, no_show, late_cancelled]booking_methodsstring[]Possible values: [membership, dropin, free]booking_sourcesstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$event_typesstring[]Possible values: [appointment, class]include_futurebooleanDefault value: falseinstructorsstringoffering_typesinteger[]venuesinteger[]updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;event_start_ltestring&lt;date-time&gt;event_start_gtestring&lt;date-time&gt;event_timeframestringpivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "customers": [    0  ],  "customer_memberships": [    0  ],  "memberships": [    0  ],  "status": [    "attended"  ],  "attendance_status": [    "attended"  ],  "booking_methods": [    "membership"  ],  "booking_sources": [    "string"  ],  "event_types": [    "appointment"  ],  "include_future": False,  "instructors": "string",  "offering_types": [    0  ],  "venues": [    0  ],  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "event_start_lte": "2024-07-29T15:51:28.071Z",  "event_start_gte": "2024-07-29T15:51:28.071Z",  "event_timeframe": "string",  "pivot": "all",  "max_pivot_columns": 4})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/attendances.grouped/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "customers": [    0  ],  "customer_memberships": [    0  ],  "memberships": [    0  ],  "status": [    "attended"  ],  "attendance_status": [    "attended"  ],  "booking_methods": [    "membership"  ],  "booking_sources": [    "string"  ],  "event_types": [    "appointment"  ],  "include_future": False,  "instructors": "string",  "offering_types": [    0  ],  "venues": [    0  ],  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "event_start_lte": "2024-07-29T15:51:28.071Z",  "event_start_gte": "2024-07-29T15:51:28.071Z",  "event_timeframe": "string",  "pivot": "all",  "max_pivot_columns": 4}
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
"event_timeframe": "string",
"pivot": "all",
"max_pivot_columns": 4
}
```


