# Endpoints_Reports Attendance Strikes Grouped Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/attendance_strikes`

## Summary
Grouped Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/attendance_strikes.grouped/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, attendance_status, attendance.status, attendance, rule_applies_to, rule.applies_to, rule, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, day_of_week, event_start_time, event.start_time, count], &gt;= 1customersinteger[]Only include infractions for particular customers.statusstring[]Only include infractions with a particular status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance_statusstring[]Only include infractions for a particular attendance status.Possible values: [late_cancel, no_show]rule_applies_tostring[]Only include infractions for rules with different applicabilities.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]membershipsinteger[]Only include infractions associated with particular memberships.offering_typesinteger[]Only include infractions for attended events with particular offering types.venuesinteger[]Only include infractions for attended events at particular venues.penaltyintegerOnly include infractions part of a sequence that triggered a particular penalty.event_starts_at_ltestring&lt;date-time&gt;event_starts_at_gtestring&lt;date-time&gt;pivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, attendance_status, attendance.status, attendance, rule_applies_to, rule.applies_to, rule, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, day_of_week, event_start_time, event.start_time, count], &gt;= 1customersinteger[]Only include infractions for particular customers.statusstring[]Only include infractions with a particular status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance_statusstring[]Only include infractions for a particular attendance status.Possible values: [late_cancel, no_show]rule_applies_tostring[]Only include infractions for rules with different applicabilities.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]membershipsinteger[]Only include infractions associated with particular memberships.offering_typesinteger[]Only include infractions for attended events with particular offering types.venuesinteger[]Only include infractions for attended events at particular venues.penaltyintegerOnly include infractions part of a sequence that triggered a particular penalty.event_starts_at_ltestring&lt;date-time&gt;event_starts_at_gtestring&lt;date-time&gt;pivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, attendance_status, attendance.status, attendance, rule_applies_to, rule.applies_to, rule, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, day_of_week, event_start_time, event.start_time, count], &gt;= 1customersinteger[]Only include infractions for particular customers.statusstring[]Only include infractions with a particular status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance_statusstring[]Only include infractions for a particular attendance status.Possible values: [late_cancel, no_show]rule_applies_tostring[]Only include infractions for rules with different applicabilities.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]membershipsinteger[]Only include infractions associated with particular memberships.offering_typesinteger[]Only include infractions for attended events with particular offering types.venuesinteger[]Only include infractions for attended events at particular venues.penaltyintegerOnly include infractions part of a sequence that triggered a particular penalty.event_starts_at_ltestring&lt;date-time&gt;event_starts_at_gtestring&lt;date-time&gt;pivotstring
Possible values: [all, year, month, week]Default value: allmax_pivot_columnsintegerPossible values: &lt;= 12Default value: 4
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "customers": [    0  ],  "status": [    "open"  ],  "attendance_status": [    "late_cancel"  ],  "rule_applies_to": [    "no_shows"  ],  "memberships": [    0  ],  "offering_types": [    0  ],  "venues": [    0  ],  "penalty": 0,  "event_starts_at_lte": "2024-07-29T15:51:28.071Z",  "event_starts_at_gte": "2024-07-29T15:51:28.071Z",  "pivot": "all",  "max_pivot_columns": 4})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/attendance_strikes.grouped/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "customers": [    0  ],  "status": [    "open"  ],  "attendance_status": [    "late_cancel"  ],  "rule_applies_to": [    "no_shows"  ],  "memberships": [    0  ],  "offering_types": [    0  ],  "venues": [    0  ],  "penalty": 0,  "event_starts_at_lte": "2024-07-29T15:51:28.071Z",  "event_starts_at_gte": "2024-07-29T15:51:28.071Z",  "pivot": "all",  "max_pivot_columns": 4}
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
"status": [
"open"
],
"attendance_status": [
"late_cancel"
],
"rule_applies_to": [
"no_shows"
],
"memberships": [
0
],
"offering_types": [
0
],
"venues": [
0
],
"penalty": 0,
"event_starts_at_lte": "2024-07-29T15:51:28.071Z",
"event_starts_at_gte": "2024-07-29T15:51:28.071Z",
"pivot": "all",
"max_pivot_columns": 4
}
```


