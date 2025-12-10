# Endpoints_Reports Attendances Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/attendances/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/attendances/data
Query Parametersattendance_status string[]Possible values: [attended, registered, no_show, late_cancelled]booking_methods string[]Possible values: [membership, dropin, free]booking_sources string[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$columns string[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_thumbnail_url, customer.thumbnail_url, event_id, event.id, event, event_starts_at, event.starts_at, event_ends_at, event.ends_at, event_name, event.name, offering_type_id, offering_type.id, offering_type, offering_type_name, offering_type.name, venue_id, venue.id, venue, venue_name, venue.name, instructors, booking_method, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_name, customer_membership.membership.name, booking_source, status, checkin_ocurred_at, checkin.ocurred_at, checkin, is_first_attendance]customer_memberships integer[]customers integer[]event_start_gte date-timeevent_start_lte date-timeevent_timeframe stringevent_types string[]Possible values: [appointment, class]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinclude_future booleanDefault value: falseinstructors stringlimit integerPossible values: &lt;= 100Default value: 50memberships integer[]offering_types integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [attended, registered, no_show, late_cancelled]updated_at_gte date-timeupdated_at_lte date-timevenues integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [idintegerThe unique identifier for the attendance.updated_atstring&lt;date-time&gt;When the attendance was last updated.customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.thumbnail_urlstringThe URL of the customer's profile picture.event objectidintegerThe event's unique identifier.starts_atstring&lt;date-time&gt;When the event starts.ends_atstring&lt;date-time&gt;When the event ends.namestringThe event's name.offering_type objectidintegerThe offering type's unique identifier.namestringThe offering type's name.venue objectidintegerThe venue's unique identifier.namestringThe venue's name.instructors object[]A list of instructors with their ID and nameArray [idintegerrequiredThe unique identifier for the instructornamestringrequiredThe name of the instructor]booking_methodstringThe method used to book the attendance (membership, drop-in, or free).customer_membership objectidintegerThe unique identifier for the customer's membership.membership objectidintegerThe unique identifier for the membership.namestringThe name of the membership.booking_sourcestringThe application or platform used to book the attendance.statusstringThe current status of the attendance (registered, attended, late cancelled, or no show).checkin objectocurred_atstring&lt;date-time&gt;The timestamp when the customer checked in for the event.is_first_attendancebooleanWhether this is the customer's first attendance at any event.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "id": 0,      "updated_at": "2024-07-29T15:51:28.071Z",      "customer": {        "id": 0,        "name": "string",        "email": "string",        "thumbnail_url": "string"      },      "event": {        "id": 0,        "starts_at": "2024-07-29T15:51:28.071Z",        "ends_at": "2024-07-29T15:51:28.071Z",        "name": "string"      },      "offering_type": {        "id": 0,        "name": "string"      },      "venue": {        "id": 0,        "name": "string"      },      "instructors": [        {          "id": 0,          "name": "string"        }      ],      "booking_method": "string",      "customer_membership": {        "id": 0,        "membership": {          "id": 0,          "name": "string"        }      },      "booking_source": "string",      "status": "string",      "checkin": {        "ocurred_at": "2024-07-29T15:51:28.071Z"      },      "is_first_attendance": true    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/attendances/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersattendance_status — queryattendedregisteredno_showlate_cancelledbooking_methods — querymembershipdropinfreebooking_sources — queryAdd itemcolumns — queryidupdated_atcustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailcustomer_thumbnail_urlcustomer.thumbnail_urlevent_idevent.ideventevent_starts_atevent.starts_atevent_ends_atevent.ends_atevent_nameevent.nameoffering_type_idoffering_type.idoffering_typeoffering_type_nameoffering_type.namevenue_idvenue.idvenuevenue_namevenue.nameinstructorsbooking_methodcustomer_membership_idcustomer_membership.idcustomer_membershipmembership_idcustomer_membership.membership.idcustomer_membership.membershipmembership_namecustomer_membership.membership.namebooking_sourcestatuscheckin_ocurred_atcheckin.ocurred_atcheckinis_first_attendancecustomer_memberships — queryAdd itemcustomers — queryAdd itemevent_start_gte — queryevent_start_lte — queryevent_timeframe — queryevent_types — queryappointmentclassformat — query---csvjsonid_gt — queryinclude_future — query---truefalseinstructors — querylimit — querymemberships — queryAdd itemoffering_types — queryAdd itemoffset — querypage — querypage_size — querysort — queryAdd itemstatus — queryattendedregisteredno_showlate_cancelledupdated_at_gte — queryupdated_at_lte — queryvenues — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousGrouped Data ExportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "id": 0,      "updated_at": "2024-07-29T15:51:28.071Z",      "customer": {        "id": 0,        "name": "string",        "email": "string",        "thumbnail_url": "string"      }
```

```json
{        "id": 0,        "starts_at": "2024-07-29T15:51:28.071Z",        "ends_at": "2024-07-29T15:51:28.071Z",        "name": "string"      }
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
{        "ocurred_at": "2024-07-29T15:51:28.071Z"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


