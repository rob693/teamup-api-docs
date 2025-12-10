# Endpoints_Reports Customer Referrals Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/customer_referrals/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/customer_referrals/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvreferring_customersinteger[]signup_customersinteger[]membershipsinteger[]statusstring[]Possible values: [pending, confirmed]signup_date_ltestring&lt;date&gt;signup_date_gtestring&lt;date&gt;signup_date_timeframeOnly return rows for referrals with a singup date within a particular timeframe. See section on timeframe syntax for formatting. (string)confirmation_date_ltestring&lt;date&gt;confirmation_date_gtestring&lt;date&gt;confirmation_date_timeframeOnly return rows for referrals that were confirmed within a particular timeframe. See section on timeframe syntax for formatting. (string)updated_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;columnsstring[]Possible values: [id, referring_customer_id, referring_customer.id, referring_customer, referrering_customer_name, referring_customer.name, referrering_customer_email, referring_customer.email, referring_customer_venue_id, referring_customer.venue.id, referring_customer.venue, referring_customer_venue_name, referring_customer.venue.name, signup_customer_id, signup_customer.id, signup_customer, signup_customer_name, signup_customer.name, signup_customer_email, signup_customer.email, customer_membership_id, signup_customer_membership.id, signup_customer_membership, customer_membership_status, signup_customer_membership.status, signup_customer_venue_id, signup_customer.venue.id, signup_customer.venue, signup_customer_venue_name, signup_customer.venue.name, membership_id, signup_customer_membership.membership.id, signup_customer_membership.membership, membership_name, signup_customer_membership.membership.name, credit_given, signup_date, confirmation_date, updated_at, status, membership_use_count, signup_customer_membership.use_count]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvreferring_customersinteger[]signup_customersinteger[]membershipsinteger[]statusstring[]Possible values: [pending, confirmed]signup_date_ltestring&lt;date&gt;signup_date_gtestring&lt;date&gt;signup_date_timeframeOnly return rows for referrals with a singup date within a particular timeframe. See section on timeframe syntax for formatting. (string)confirmation_date_ltestring&lt;date&gt;confirmation_date_gtestring&lt;date&gt;confirmation_date_timeframeOnly return rows for referrals that were confirmed within a particular timeframe. See section on timeframe syntax for formatting. (string)updated_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;columnsstring[]Possible values: [id, referring_customer_id, referring_customer.id, referring_customer, referrering_customer_name, referring_customer.name, referrering_customer_email, referring_customer.email, referring_customer_venue_id, referring_customer.venue.id, referring_customer.venue, referring_customer_venue_name, referring_customer.venue.name, signup_customer_id, signup_customer.id, signup_customer, signup_customer_name, signup_customer.name, signup_customer_email, signup_customer.email, customer_membership_id, signup_customer_membership.id, signup_customer_membership, customer_membership_status, signup_customer_membership.status, signup_customer_venue_id, signup_customer.venue.id, signup_customer.venue, signup_customer_venue_name, signup_customer.venue.name, membership_id, signup_customer_membership.membership.id, signup_customer_membership.membership, membership_name, signup_customer_membership.membership.name, credit_given, signup_date, confirmation_date, updated_at, status, membership_use_count, signup_customer_membership.use_count]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvreferring_customersinteger[]signup_customersinteger[]membershipsinteger[]statusstring[]Possible values: [pending, confirmed]signup_date_ltestring&lt;date&gt;signup_date_gtestring&lt;date&gt;signup_date_timeframeOnly return rows for referrals with a singup date within a particular timeframe. See section on timeframe syntax for formatting. (string)confirmation_date_ltestring&lt;date&gt;confirmation_date_gtestring&lt;date&gt;confirmation_date_timeframeOnly return rows for referrals that were confirmed within a particular timeframe. See section on timeframe syntax for formatting. (string)updated_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;columnsstring[]Possible values: [id, referring_customer_id, referring_customer.id, referring_customer, referrering_customer_name, referring_customer.name, referrering_customer_email, referring_customer.email, referring_customer_venue_id, referring_customer.venue.id, referring_customer.venue, referring_customer_venue_name, referring_customer.venue.name, signup_customer_id, signup_customer.id, signup_customer, signup_customer_name, signup_customer.name, signup_customer_email, signup_customer.email, customer_membership_id, signup_customer_membership.id, signup_customer_membership, customer_membership_status, signup_customer_membership.status, signup_customer_venue_id, signup_customer.venue.id, signup_customer.venue, signup_customer_venue_name, signup_customer.venue.name, membership_id, signup_customer_membership.membership.id, signup_customer_membership.membership, membership_name, signup_customer_membership.membership.name, credit_given, signup_date, confirmation_date, updated_at, status, membership_use_count, signup_customer_membership.use_count]
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "referring_customers": [    0  ],  "signup_customers": [    0  ],  "memberships": [    0  ],  "status": [    "pending"  ],  "signup_date_lte": "2024-07-29",  "signup_date_gte": "2024-07-29",  "signup_date_timeframe": "string",  "confirmation_date_lte": "2024-07-29",  "confirmation_date_gte": "2024-07-29",  "confirmation_date_timeframe": "string",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "columns": [    "id"  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/customer_referrals/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "referring_customers": [    0  ],  "signup_customers": [    0  ],  "memberships": [    0  ],  "status": [    "pending"  ],  "signup_date_lte": "2024-07-29",  "signup_date_gte": "2024-07-29",  "signup_date_timeframe": "string",  "confirmation_date_lte": "2024-07-29",  "confirmation_date_gte": "2024-07-29",  "confirmation_date_timeframe": "string",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "columns": [    "id"  ]}
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
"referring_customers": [
0
],
"signup_customers": [
0
],
"memberships": [
0
],
"status": [
"pending"
],
"signup_date_lte": "2024-07-29",
"signup_date_gte": "2024-07-29",
"signup_date_timeframe": "string",
"confirmation_date_lte": "2024-07-29",
"confirmation_date_gte": "2024-07-29",
"confirmation_date_timeframe": "string",
"updated_at_gte": "2024-07-29T15:51:28.071Z",
"updated_at_lte": "2024-07-29T15:51:28.071Z",
"columns": [
"id"
]
}
```


