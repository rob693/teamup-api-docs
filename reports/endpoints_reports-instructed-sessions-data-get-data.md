# Endpoints_Reports Instructed Sessions Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/instructed_sessions/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/instructed_sessions/data
Query Parameterscolumns string[]Possible values: [id, name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, instructor_thumbnail_url, instructor.thumbnail_url, starts_at, venue_id, venue.id, venue, venue_name, venue.name, venue_timezone, max_occupancy, hours, attended_count, no_show_count, late_cancel_count, attended_comped_count, comped_counts.attended, comped_counts, session_type, instructor_pay_rate_id, instructor_pay_rate.id, instructor_pay_rate, instructor_pay_rate_name, instructor_pay_rate.name, instructor_pay_rate_type, instructor_pay_rate.type, instructor_pay_rate_base, instructor_pay_rate.base, instructor_pay, pay_rate_tiers, instructor_pay_rate.tiers, instructor_pay_calculation_pending]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinstructors stringlimit integerPossible values: &lt;= 100Default value: 50offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.pay_rates integer[]session_types string[]Possible values: [class, course_session]sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.starts_at_gte date-timestarts_at_lte date-timetimeframe stringvenues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [idintegerThe unique identifier for the instructed session.namestringThe name of the session (event or course).offering_type objectidintegerThe unique identifier for the offering type.namestringThe name of the offering type.instructor objectidintegerThe unique identifier for the instructor.namestringThe name of the instructor.thumbnail_urlstringThe URL of the instructor's profile thumbnail image.starts_atstringThe start date and time of the session.venue objectidintegerThe unique identifier for the venue.namestringThe name of the venue.venue_timezonestringThe timezone of the venue.max_occupancyintegerThe maximum number of participants allowed in the session.hoursnumberThe duration of the session in hours.attended_countintegerThe number of participants who attended the session.no_show_countintegerThe number of participants who did not show up for the session.late_cancel_countintegerThe number of late cancellations for the session.comped_counts objectattendedintegerThe number of participants who attended with a comped (free) booking.session_typestringThe type of session: 'class' for events or 'course_session' for course dates.instructor_pay_rate objectidintegerThe unique identifier for the instructor's pay rate.namestringThe name of the instructor's pay rate.typestringThe type of instructor pay rate (per_customer, per_hour, or per_customer_tiered).basestringThe base rate amount for instructor pay.tiers object[]The tiered pay rate structure for per_customer_tiered pay rates.Array [upper_boundnumber | nullnullablelower_boundnumberper_customer_amount objectamountnumbercurrencystring]instructor_pay objectThe calculated pay amount for the instructor.decimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]instructor_pay_calculation_pendingbooleanWhether the instructor pay calculation is still pending.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "id": 0,      "name": "string",      "offering_type": {        "id": 0,        "name": "string"      },      "instructor": {        "id": 0,        "name": "string",        "thumbnail_url": "string"      },      "starts_at": "string",      "venue": {        "id": 0,        "name": "string"      },      "venue_timezone": "string",      "max_occupancy": 0,      "hours": 0,      "attended_count": 0,      "no_show_count": 0,      "late_cancel_count": 0,      "comped_counts": {        "attended": 0      },      "session_type": "string",      "instructor_pay_rate": {        "id": 0,        "name": "string",        "type": "string",        "base": "string",        "tiers": [          {            "upper_bound": 0,            "lower_bound": 0,            "per_customer_amount": {              "amount": 0,              "currency": "string"            }          }        ]      },      "instructor_pay": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "instructor_pay_calculation_pending": true    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/instructed_sessions/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscolumns — queryidnameoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.nameinstructor_idinstructor.idinstructorinstructor_nameinstructor.nameinstructor_thumbnail_urlinstructor.thumbnail_urlstarts_atvenue_idvenue.idvenuevenue_namevenue.namevenue_timezonemax_occupancyhoursattended_countno_show_countlate_cancel_countattended_comped_countcomped_counts.attendedcomped_countssession_typeinstructor_pay_rate_idinstructor_pay_rate.idinstructor_pay_rateinstructor_pay_rate_nameinstructor_pay_rate.nameinstructor_pay_rate_typeinstructor_pay_rate.typeinstructor_pay_rate_baseinstructor_pay_rate.baseinstructor_paypay_rate_tiersinstructor_pay_rate.tiersinstructor_pay_calculation_pendingformat — query---csvjsonid_gt — queryinstructors — querylimit — queryoffering_types — queryAdd itemoffset — querypage — querypage_size — querypay_rates — queryAdd itemsession_types — queryclasscourse_sessionsort — queryAdd itemstarts_at_gte — querystarts_at_lte — querytimeframe — queryvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousInstructed Sessions ReportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "id": 0,      "name": "string",      "offering_type": {        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string",        "thumbnail_url": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "attended": 0      }
```

```json
{        "id": 0,        "name": "string",        "type": "string",        "base": "string",        "tiers": [          {            "upper_bound": 0,            "lower_bound": 0,            "per_customer_amount": {              "amount": 0,              "currency": "string"            }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


