# Endpoints_Reports Course Session Attendances Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/course_session_attendances/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/course_session_attendances/data
Query Parametersbooking_methods string[]Possible values: [session_dropin, membership, course_dropin]columns string[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, course_session_id, course_session.id, course_session, course_session_starts_at, course_session.starts_at, course_id, course.id, course, course_name, course.name, course_series_id, course_series.id, course_series, course_series_name, course_series.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, is_makeup, status]customers integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinclude_future booleanDefault value: falseinstructors stringis_makeup booleanlimit integerPossible values: &lt;= 100Default value: 50memberships integer[]offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.session_starts_at_gte date-timesession_starts_at_lte date-timesession_timeframe stringsort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [no_show, registered, attended]venues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.course_session objectidintegerThe unique identifier for the course session.starts_atstring&lt;date-time&gt;The start date and time of the course session.course objectidintegerThe unique identifier for the course.namestringThe name of the course.course_series objectidintegerThe unique identifier for the course series.namestringThe name of the course series.offering_type objectidintegerThe unique identifier for the offering type.namestringThe name of the offering type.venue objectidintegerThe unique identifier for the venue.namestringThe name of the venue.instructors object[]A list of instructors with their ID and nameArray [idintegerrequiredThe unique identifier for the instructornamestringrequiredThe name of the instructor]booking_methodstringThe method used to book this attendance (membership, session drop-in, course drop-in).customer_membership objectidintegerThe unique identifier for the customer membership.membership objectidintegerThe unique identifier for the membership type.namestringThe name of the membership type.is_makeupbooleanWhether this attendance is for a makeup session.statusstringThe attendance status (attended, no_show, registered).]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "course_session": {        "id": 0,        "starts_at": "2024-07-29T15:51:28.071Z"      },      "course": {        "id": 0,        "name": "string"      },      "course_series": {        "id": 0,        "name": "string"      },      "offering_type": {        "id": 0,        "name": "string"      },      "venue": {        "id": 0,        "name": "string"      },      "instructors": [        {          "id": 0,          "name": "string"        }      ],      "booking_method": "string",      "customer_membership": {        "id": 0,        "membership": {          "id": 0,          "name": "string"        }      },      "is_makeup": true,      "status": "string"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/course_session_attendances/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersbooking_methods — querysession_dropinmembershipcourse_dropincolumns — querycustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailcourse_session_idcourse_session.idcourse_sessioncourse_session_starts_atcourse_session.starts_atcourse_idcourse.idcoursecourse_namecourse.namecourse_series_idcourse_series.idcourse_seriescourse_series_namecourse_series.nameoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.namevenue_idvenue.idvenuevenue_namevenue.nameinstructorsbooking_methodcustomer_membership_idcustomer_membership.idcustomer_membershipmembership_idcustomer_membership.membership.idcustomer_membership.membershipmembership_namecustomer_membership.membership.nameis_makeupstatuscustomers — queryAdd itemformat — query---csvjsonid_gt — queryinclude_future — query---truefalseinstructors — queryis_makeup — query---truefalselimit — querymemberships — queryAdd itemoffering_types — queryAdd itemoffset — querypage — querypage_size — querysession_starts_at_gte — querysession_starts_at_lte — querysession_timeframe — querysort — queryAdd itemstatus — queryno_showregisteredattendedvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousGrouped Data ExportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "id": 0,        "starts_at": "2024-07-29T15:51:28.071Z"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{          "id": 0,          "name": "string"        }
```

```json
{        "id": 0,        "membership": {          "id": 0,          "name": "string"        }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


