# Endpoints_Reports Attendances Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/attendances`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/attendances.grouped/data
Query Parametersattendance_status string[]Possible values: [attended, registered, no_show, late_cancelled]booking_methods string[]Possible values: [membership, dropin, free]booking_sources string[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$columns string[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, day_of_week, event_start_time, event.start_time, event, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, booking_method, booking_source, status, count], &gt;= 1customer_memberships integer[]customers integer[]event_start_gte date-timeevent_start_lte date-timeevent_timeframe stringevent_types string[]Possible values: [appointment, class]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinclude_future booleanDefault value: falseinstructors stringlimit integerPossible values: &lt;= 100Default value: 50max_pivot_columns integerPossible values: &lt;= 12Default value: 4memberships integer[]offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.pivot stringPossible values: non-empty, [all, year, month, week]
Default value: allsort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [attended, registered, no_show, late_cancelled]updated_at_gte date-timeupdated_at_lte date-timevenues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.day_of_weekstringThe day of the week when the event occurred.event objectstart_timestringThe start time of the event (without date).offering_type objectidintegerThe offering type's unique identifier.namestringThe offering type's name.venue objectidintegerThe venue's unique identifier.namestringThe venue's name.booking_methodstringThe method used to book the attendance (membership, drop-in, or free).booking_sourcestringThe application or platform used to book the attendance.statusstringThe current status of the attendance (registered, attended, late cancelled, or no show).countintegerThe number of attendances in the group.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "day_of_week": "string",      "event": {        "start_time": "string"      },      "offering_type": {        "id": 0,        "name": "string"      },      "venue": {        "id": 0,        "name": "string"      },      "booking_method": "string",      "booking_source": "string",      "status": "string",      "count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/attendances.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredcustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailday_of_weekevent_start_timeevent.start_timeeventoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.namevenue_idvenue.idvenuevenue_namevenue.namebooking_methodbooking_sourcestatuscountShow optional parametersattendance_status — queryattendedregisteredno_showlate_cancelledbooking_methods — querymembershipdropinfreebooking_sources — queryAdd itemcustomer_memberships — queryAdd itemcustomers — queryAdd itemevent_start_gte — queryevent_start_lte — queryevent_timeframe — queryevent_types — queryappointmentclassformat — query---csvjsonid_gt — queryinclude_future — query---truefalseinstructors — querylimit — querymax_pivot_columns — querymemberships — queryAdd itemoffering_types — queryAdd itemoffset — querypage — querypage_size — querypivot — query---allyearmonthweeksort — queryAdd itemstatus — queryattendedregisteredno_showlate_cancelledupdated_at_gte — queryupdated_at_lte — queryvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousAttendances ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "start_time": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


