# Endpoints_Reports Attendance Strikes Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/attendance_strikes/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/attendance_strikes/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, status, rule_applies_to, rule.applies_to, rule, penalty_rule_max_infractions, rule.max_infractions, penalty_rule_days, rule.days, penalty_system_id, rule.system.id, rule.system, penalty_system_name, rule.system.name, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, event_type, event.type, event_starts_at, event.starts_at, attendance_status, attendance.status, attendance, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, sequence_position, penalty_charge_amount, penalty.charge.amount, penalty, penalty.charge, penalty_charge_due_date, penalty.charge.due_date, penalty_id, penalty.id]customersinteger[]Only include infractions for particular customers.statusstring[]Only include infractions with a particular status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance_statusstring[]Only include infractions for a particular attendance status.Possible values: [late_cancel, no_show]rule_applies_tostring[]Only include infractions for rules with different applicabilities.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]membershipsinteger[]Only include infractions associated with particular memberships.offering_typesinteger[]Only include infractions for attended events with particular offering types.venuesinteger[]Only include infractions for attended events at particular venues.penaltyintegerOnly include infractions part of a sequence that triggered a particular penalty.event_starts_at_ltestring&lt;date-time&gt;event_starts_at_gtestring&lt;date-time&gt;Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, status, rule_applies_to, rule.applies_to, rule, penalty_rule_max_infractions, rule.max_infractions, penalty_rule_days, rule.days, penalty_system_id, rule.system.id, rule.system, penalty_system_name, rule.system.name, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, event_type, event.type, event_starts_at, event.starts_at, attendance_status, attendance.status, attendance, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, sequence_position, penalty_charge_amount, penalty.charge.amount, penalty, penalty.charge, penalty_charge_due_date, penalty.charge.due_date, penalty_id, penalty.id]customersinteger[]Only include infractions for particular customers.statusstring[]Only include infractions with a particular status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance_statusstring[]Only include infractions for a particular attendance status.Possible values: [late_cancel, no_show]rule_applies_tostring[]Only include infractions for rules with different applicabilities.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]membershipsinteger[]Only include infractions associated with particular memberships.offering_typesinteger[]Only include infractions for attended events with particular offering types.venuesinteger[]Only include infractions for attended events at particular venues.penaltyintegerOnly include infractions part of a sequence that triggered a particular penalty.event_starts_at_ltestring&lt;date-time&gt;event_starts_at_gtestring&lt;date-time&gt;Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, status, rule_applies_to, rule.applies_to, rule, penalty_rule_max_infractions, rule.max_infractions, penalty_rule_days, rule.days, penalty_system_id, rule.system.id, rule.system, penalty_system_name, rule.system.name, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, event_type, event.type, event_starts_at, event.starts_at, attendance_status, attendance.status, attendance, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, sequence_position, penalty_charge_amount, penalty.charge.amount, penalty, penalty.charge, penalty_charge_due_date, penalty.charge.due_date, penalty_id, penalty.id]customersinteger[]Only include infractions for particular customers.statusstring[]Only include infractions with a particular status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance_statusstring[]Only include infractions for a particular attendance status.Possible values: [late_cancel, no_show]rule_applies_tostring[]Only include infractions for rules with different applicabilities.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]membershipsinteger[]Only include infractions associated with particular memberships.offering_typesinteger[]Only include infractions for attended events with particular offering types.venuesinteger[]Only include infractions for attended events at particular venues.penaltyintegerOnly include infractions part of a sequence that triggered a particular penalty.event_starts_at_ltestring&lt;date-time&gt;event_starts_at_gtestring&lt;date-time&gt;
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "customers": [    0  ],  "status": [    "open"  ],  "attendance_status": [    "late_cancel"  ],  "rule_applies_to": [    "no_shows"  ],  "memberships": [    0  ],  "offering_types": [    0  ],  "venues": [    0  ],  "penalty": 0,  "event_starts_at_lte": "2024-07-29T15:51:28.071Z",  "event_starts_at_gte": "2024-07-29T15:51:28.071Z"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/attendance_strikes/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "customers": [    0  ],  "status": [    "open"  ],  "attendance_status": [    "late_cancel"  ],  "rule_applies_to": [    "no_shows"  ],  "memberships": [    0  ],  "offering_types": [    0  ],  "venues": [    0  ],  "penalty": 0,  "event_starts_at_lte": "2024-07-29T15:51:28.071Z",  "event_starts_at_gte": "2024-07-29T15:51:28.071Z"}
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
"event_starts_at_gte": "2024-07-29T15:51:28.071Z"
}
```


