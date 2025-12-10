# Endpoints_Reports Classes Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/classes/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/classes/data
Query Parameterscolumns string[]Possible values: [id, starts_at, updated_at, status, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, start_time, duration_minutes, day_of_week, attendance_count, late_cancel_count, no_show_count]day_of_week string[]Possible values: [sunday, monday, tuesday, wednesday, thursday, friday, staturday]durations integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinclude_future booleanDefault value: falseinstructors stringlimit integerPossible values: &lt;= 100Default value: 50offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.starts_at_gte date-timestarts_at_lte date-timestatus stringtimeframe stringupdated_at_gte date-timeupdated_at_lte date-timevenues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [idintegerThe unique identifier for the class.starts_atstring&lt;date-time&gt;When the class starts.updated_atstring&lt;date-time&gt;When the class was last updated.statusstringThe current status of the class (active or cancelled).offering_type objectidintegerThe unique identifier for the offering type of the class.namestringThe name of the offering type of the class.venue objectidintegerThe unique identifier for the venue where the class takes place.namestringThe name of the venue where the class takes place.instructors object[]A list of instructors with their ID and nameArray [idintegerrequiredThe unique identifier for the instructornamestringrequiredThe name of the instructor]start_timestringThe start time of the class (without date).duration_minutesintegerThe duration of the class in minutes.day_of_weekstringThe day of the week when the class occurs.attendance_countintegerThe number of attendees for the class.late_cancel_countintegerThe number of late cancellations for the class.no_show_countintegerThe number of no-shows for the class.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "id": 0,      "starts_at": "2024-07-29T15:51:28.071Z",      "updated_at": "2024-07-29T15:51:28.071Z",      "status": "string",      "offering_type": {        "id": 0,        "name": "string"      },      "venue": {        "id": 0,        "name": "string"      },      "instructors": [        {          "id": 0,          "name": "string"        }      ],      "start_time": "string",      "duration_minutes": 0,      "day_of_week": "string",      "attendance_count": 0,      "late_cancel_count": 0,      "no_show_count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/classes/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscolumns — queryidstarts_atupdated_atstatusoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.namevenue_idvenue.idvenuevenue_namevenue.nameinstructorsstart_timeduration_minutesday_of_weekattendance_countlate_cancel_countno_show_countday_of_week — querysundaymondaytuesdaywednesdaythursdayfridaystaturdaydurations — queryAdd itemformat — query---csvjsonid_gt — queryinclude_future — query---truefalseinstructors — querylimit — queryoffering_types — queryAdd itemoffset — querypage — querypage_size — querysort — queryAdd itemstarts_at_gte — querystarts_at_lte — querystatus — querytimeframe — queryupdated_at_gte — queryupdated_at_lte — queryvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousGrouped Data ExportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "id": 0,      "starts_at": "2024-07-29T15:51:28.071Z",      "updated_at": "2024-07-29T15:51:28.071Z",      "status": "string",      "offering_type": {        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{          "id": 0,          "name": "string"        }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


