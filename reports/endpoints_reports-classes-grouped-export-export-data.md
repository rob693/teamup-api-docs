# Endpoints_Reports Classes Grouped Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/classes`

## Summary
Grouped Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/classes.grouped/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvinstructorsstringoffering_typesinteger[]venuesinteger[]day_of_weekstring[]Possible values: [sunday, monday, tuesday, wednesday, thursday, friday, staturday]statusstringstarts_at_ltestring&lt;date-time&gt;starts_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;timeframestringdurationsinteger[]include_futurebooleanDefault value: falsecolumnsstring[]requiredPossible values: [start_time, day_of_week, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, duration_minutes, instructor_id, instructor.id, instructor, instructor_name, instructor.name, year, month, average_attendees, count], &gt;= 1Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvinstructorsstringoffering_typesinteger[]venuesinteger[]day_of_weekstring[]Possible values: [sunday, monday, tuesday, wednesday, thursday, friday, staturday]statusstringstarts_at_ltestring&lt;date-time&gt;starts_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;timeframestringdurationsinteger[]include_futurebooleanDefault value: falsecolumnsstring[]requiredPossible values: [start_time, day_of_week, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, duration_minutes, instructor_id, instructor.id, instructor, instructor_name, instructor.name, year, month, average_attendees, count], &gt;= 1Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvinstructorsstringoffering_typesinteger[]venuesinteger[]day_of_weekstring[]Possible values: [sunday, monday, tuesday, wednesday, thursday, friday, staturday]statusstringstarts_at_ltestring&lt;date-time&gt;starts_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;timeframestringdurationsinteger[]include_futurebooleanDefault value: falsecolumnsstring[]requiredPossible values: [start_time, day_of_week, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, duration_minutes, instructor_id, instructor.id, instructor, instructor_name, instructor.name, year, month, average_attendees, count], &gt;= 1
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "instructors": "string",  "offering_types": [    0  ],  "venues": [    0  ],  "day_of_week": [    "sunday"  ],  "status": "string",  "starts_at_lte": "2024-07-29T15:51:28.071Z",  "starts_at_gte": "2024-07-29T15:51:28.071Z",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "timeframe": "string",  "durations": [    0  ],  "include_future": False,  "columns": [    "start_time"  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/classes.grouped/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "instructors": "string",  "offering_types": [    0  ],  "venues": [    0  ],  "day_of_week": [    "sunday"  ],  "status": "string",  "starts_at_lte": "2024-07-29T15:51:28.071Z",  "starts_at_gte": "2024-07-29T15:51:28.071Z",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "timeframe": "string",  "durations": [    0  ],  "include_future": False,  "columns": [    "start_time"  ]}
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
"instructors": "string",
"offering_types": [
0
],
"venues": [
0
],
"day_of_week": [
"sunday"
],
"status": "string",
"starts_at_lte": "2024-07-29T15:51:28.071Z",
"starts_at_gte": "2024-07-29T15:51:28.071Z",
"updated_at_lte": "2024-07-29T15:51:28.071Z",
"updated_at_gte": "2024-07-29T15:51:28.071Z",
"timeframe": "string",
"durations": [
0
],
"include_future": false,
"columns": [
"start_time"
]
}
```


