# Endpoints_Reports Classes Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/classes`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/classes.grouped/data
Query Parameterscolumns string[]requiredPossible values: [start_time, day_of_week, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, duration_minutes, instructor_id, instructor.id, instructor, instructor_name, instructor.name, year, month, average_attendees, count], &gt;= 1day_of_week string[]Possible values: [sunday, monday, tuesday, wednesday, thursday, friday, staturday]durations integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinclude_future booleanDefault value: falseinstructors stringlimit integerPossible values: &lt;= 100Default value: 50offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.starts_at_gte date-timestarts_at_lte date-timestatus stringtimeframe stringupdated_at_gte date-timeupdated_at_lte date-timevenues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [start_timestringThe start time of the class (without date).day_of_weekstringThe day of the week when the class occurs.offering_type objectidintegerThe unique identifier for the offering type of the class.namestringThe name of the offering type of the class.venue objectidintegerThe unique identifier for the venue where the class takes place.namestringThe name of the venue where the class takes place.duration_minutesintegerThe duration of the class in minutes.instructor objectidintegerThe unique identifier for the instructor (used for grouping).namestringThe name of the instructor (used for grouping).yearintegerThe year when the class occurs (used for grouping).monthintegerThe month when the class occurs (used for grouping).average_attendeesnumberThe average number of attendees across all classes in the group.countintegerThe number of classes in the group.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "start_time": "string",      "day_of_week": "string",      "offering_type": {        "id": 0,        "name": "string"      },      "venue": {        "id": 0,        "name": "string"      },      "duration_minutes": 0,      "instructor": {        "id": 0,        "name": "string"      },      "year": 0,      "month": 0,      "average_attendees": 0,      "count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/classes.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredstart_timeday_of_weekoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.namevenue_idvenue.idvenuevenue_namevenue.nameduration_minutesinstructor_idinstructor.idinstructorinstructor_nameinstructor.nameyearmonthaverage_attendeescountShow optional parametersday_of_week — querysundaymondaytuesdaywednesdaythursdayfridaystaturdaydurations — queryAdd itemformat — query---csvjsonid_gt — queryinclude_future — query---truefalseinstructors — querylimit — queryoffering_types — queryAdd itemoffset — querypage — querypage_size — querysort — queryAdd itemstarts_at_gte — querystarts_at_lte — querystatus — querytimeframe — queryupdated_at_gte — queryupdated_at_lte — queryvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousClasses ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "start_time": "string",      "day_of_week": "string",      "offering_type": {        "id": 0,        "name": "string"      }
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


