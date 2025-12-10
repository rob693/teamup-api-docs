# Endpoints_Reports Attendance Strikes Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/attendance_strikes`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/attendance_strikes.grouped/data
Query Parametersattendance_status string[]Possible values: [late_cancel, no_show]Only include infractions for a particular attendance status.columns string[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, attendance_status, attendance.status, attendance, rule_applies_to, rule.applies_to, rule, offering_type_id, event.offering_type.id, event, event.offering_type, offering_type_name, event.offering_type.name, venue_id, event.venue.id, event.venue, venue_name, event.venue.name, membership_id, customer_membership.membership.id, customer_membership, customer_membership.membership, membership_name, customer_membership.membership.name, day_of_week, event_start_time, event.start_time, count], &gt;= 1customers integer[]Only include infractions for particular customers.event_starts_at_gte date-timeevent_starts_at_lte date-timeformat stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerPossible values: &lt;= 100Default value: 50max_pivot_columns integerPossible values: &lt;= 12Default value: 4memberships integer[]Only include infractions associated with particular memberships.offering_types integer[]Only include infractions for attended events with particular offering types.offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.penalty integerOnly include infractions part of a sequence that triggered a particular penalty.pivot stringPossible values: non-empty, [all, year, month, week]
Default value: allrule_applies_to string[]Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]Only include infractions for rules with different applicabilities.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]Only include infractions with a particular status.venues integer[]Only include infractions for attended events at particular venues.
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe customer's unique identifier.namestringThe customer's name.emailstringThe customer's email.statusstringThe attendance infraction's status.Possible values: [open, voided, expired, in_penalty_sequence, upcoming_charge, charged, charge_skipped]attendance objectstatusstringThe status of the associated attendance.Possible values: [late_cancel, no_show]rule objectapplies_tostringWhether the rule applies to late-cancels, no-shows or both.Possible values: [no_shows, late_cancels, late_cancels_or_no_shows]event objectoffering_type objectidintegerThe unqiue identifier of the event's offering type.namestringThe name of the event's offering type.venue objectidintegerThe unique identifier of the event's venue.namestringThe name of the event's venue.start_timestringThe event's start time (without a date).customer_membership objectmembership objectidintegerThe unique identifier of the membership.namestringThe name of the membership.day_of_weekstringThe day of the week when the infraction occurred.countintegerThe number of infractions in the group.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "status": "open",      "attendance": {        "status": "late_cancel"      },      "rule": {        "applies_to": "no_shows"      },      "event": {        "offering_type": {          "id": 0,          "name": "string"        },        "venue": {          "id": 0,          "name": "string"        },        "start_time": "string"      },      "customer_membership": {        "membership": {          "id": 0,          "name": "string"        }      },      "day_of_week": "string",      "count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/attendance_strikes.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredcustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailstatusattendance_statusattendance.statusattendancerule_applies_torule.applies_toruleoffering_type_idevent.offering_type.ideventevent.offering_typeoffering_type_nameevent.offering_type.namevenue_idevent.venue.idevent.venuevenue_nameevent.venue.namemembership_idcustomer_membership.membership.idcustomer_membershipcustomer_membership.membershipmembership_namecustomer_membership.membership.nameday_of_weekevent_start_timeevent.start_timecountShow optional parametersattendance_status — querylate_cancelno_showcustomers — queryAdd itemevent_starts_at_gte — queryevent_starts_at_lte — queryformat — query---csvjsonid_gt — querylimit — querymax_pivot_columns — querymemberships — queryAdd itemoffering_types — queryAdd itemoffset — querypage — querypage_size — querypenalty — querypivot — query---allyearmonthweekrule_applies_to — queryno_showslate_cancelslate_cancels_or_no_showssort — queryAdd itemstatus — queryopenvoidedexpiredin_penalty_sequenceupcoming_chargechargedcharge_skippedvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousAttendance Strikes ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "status": "late_cancel"      }
```

```json
{        "applies_to": "no_shows"      }
```

```json
{        "offering_type": {          "id": 0,          "name": "string"        }
```

```json
{          "id": 0,          "name": "string"        }
```

```json
{        "membership": {          "id": 0,          "name": "string"        }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


