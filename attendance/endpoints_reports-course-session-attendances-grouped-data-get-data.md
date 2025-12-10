# Endpoints_Reports Course Session Attendances Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/course_session_attendances`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/course_session_attendances.grouped/data
Query Parametersbooking_methods string[]Possible values: [session_dropin, membership, course_dropin]columns string[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, venue_id, venue.id, venue, venue_name, venue.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, booking_method, is_makeup, status, course_session_start_time, course_session.start_time, course_session, day_of_week, count], &gt;= 1customers integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinclude_future booleanDefault value: falseinstructors stringis_makeup booleanlimit integerPossible values: &lt;= 100Default value: 50max_pivot_columns integerPossible values: &lt;= 12Default value: 4memberships integer[]offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.pivot stringPossible values: non-empty, [all, year, month, week]
Default value: allsession_starts_at_gte date-timesession_starts_at_lte date-timesession_timeframe stringsort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [no_show, registered, attended]venues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.venue objectidintegerThe unique identifier for the venue.namestringThe name of the venue.offering_type objectidintegerThe unique identifier for the offering type.namestringThe name of the offering type.booking_methodstringThe method used to book this attendance (membership, session drop-in, course drop-in).is_makeupbooleanWhether this attendance is for a makeup session.statusstringThe attendance status (attended, no_show, registered).course_session objectstart_timestringThe start time of the course session.day_of_weekstringThe day of the week for the course session.countintegerThe count of attendances.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "venue": {        "id": 0,        "name": "string"      },      "offering_type": {        "id": 0,        "name": "string"      },      "booking_method": "string",      "is_makeup": true,      "status": "string",      "course_session": {        "start_time": "string"      },      "day_of_week": "string",      "count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/course_session_attendances.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredcustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailvenue_idvenue.idvenuevenue_namevenue.nameoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.namebooking_methodis_makeupstatuscourse_session_start_timecourse_session.start_timecourse_sessionday_of_weekcountShow optional parametersbooking_methods — querysession_dropinmembershipcourse_dropincustomers — queryAdd itemformat — query---csvjsonid_gt — queryinclude_future — query---truefalseinstructors — queryis_makeup — query---truefalselimit — querymax_pivot_columns — querymemberships — queryAdd itemoffering_types — queryAdd itemoffset — querypage — querypage_size — querypivot — query---allyearmonthweeksession_starts_at_gte — querysession_starts_at_lte — querysession_timeframe — querysort — queryAdd itemstatus — queryno_showregisteredattendedvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCourse Session Attendances ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "start_time": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


