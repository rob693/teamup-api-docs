# Endpoints_Reports Customer Membership Holds Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/customer_membership_holds/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/customer_membership_holds/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcustomersinteger[]membershipsinteger[]membership_typesstring[]Possible values: [pack, prepaid, recurring]created_at_ltestring&lt;date&gt;created_at_gtestring&lt;date&gt;updated_at_ltestring&lt;date&gt;updated_at_gtestring&lt;date&gt;created_at_timeframeOnly include holds created within a timeframe. (string)start_date_ltestring&lt;date&gt;start_date_gtestring&lt;date&gt;start_timeframeOnly include holds starting within a timeframe. (string)end_date_ltestring&lt;date&gt;end_date_gtestring&lt;date&gt;end_timeframeOnly include holds ending within a timeframe. (string)statusstring[]Possible values: [active, ended, upcoming]payment_resolution_typestring[]Possible values: [charge, credit, none]is_usage_proratedInclude holds based on whether they are prorated or not. (boolean)columnsstring[]Possible values: [id, created_at, updated_at, start_date, end_date, status, is_usage_prorated, credit_amount, reactivation_charge_amount, is_payment_resolution_customized, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_type, customer_membership.membership.type, membership_name, customer_membership.membership.name, membership_start_date, customer_membership.start_date, membership_expiration_date, customer_membership.expiration_date, membership_allowed_cancellation_date, customer_membership.allowed_cancellation_date, previous_expiration_date, previous_allowed_cancellation_date, other_active_customer_memberships, days_to_add]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcustomersinteger[]membershipsinteger[]membership_typesstring[]Possible values: [pack, prepaid, recurring]created_at_ltestring&lt;date&gt;created_at_gtestring&lt;date&gt;updated_at_ltestring&lt;date&gt;updated_at_gtestring&lt;date&gt;created_at_timeframeOnly include holds created within a timeframe. (string)start_date_ltestring&lt;date&gt;start_date_gtestring&lt;date&gt;start_timeframeOnly include holds starting within a timeframe. (string)end_date_ltestring&lt;date&gt;end_date_gtestring&lt;date&gt;end_timeframeOnly include holds ending within a timeframe. (string)statusstring[]Possible values: [active, ended, upcoming]payment_resolution_typestring[]Possible values: [charge, credit, none]is_usage_proratedInclude holds based on whether they are prorated or not. (boolean)columnsstring[]Possible values: [id, created_at, updated_at, start_date, end_date, status, is_usage_prorated, credit_amount, reactivation_charge_amount, is_payment_resolution_customized, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_type, customer_membership.membership.type, membership_name, customer_membership.membership.name, membership_start_date, customer_membership.start_date, membership_expiration_date, customer_membership.expiration_date, membership_allowed_cancellation_date, customer_membership.allowed_cancellation_date, previous_expiration_date, previous_allowed_cancellation_date, other_active_customer_memberships, days_to_add]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcustomersinteger[]membershipsinteger[]membership_typesstring[]Possible values: [pack, prepaid, recurring]created_at_ltestring&lt;date&gt;created_at_gtestring&lt;date&gt;updated_at_ltestring&lt;date&gt;updated_at_gtestring&lt;date&gt;created_at_timeframeOnly include holds created within a timeframe. (string)start_date_ltestring&lt;date&gt;start_date_gtestring&lt;date&gt;start_timeframeOnly include holds starting within a timeframe. (string)end_date_ltestring&lt;date&gt;end_date_gtestring&lt;date&gt;end_timeframeOnly include holds ending within a timeframe. (string)statusstring[]Possible values: [active, ended, upcoming]payment_resolution_typestring[]Possible values: [charge, credit, none]is_usage_proratedInclude holds based on whether they are prorated or not. (boolean)columnsstring[]Possible values: [id, created_at, updated_at, start_date, end_date, status, is_usage_prorated, credit_amount, reactivation_charge_amount, is_payment_resolution_customized, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, customer_membership_id, customer_membership.id, customer_membership, membership_id, customer_membership.membership.id, customer_membership.membership, membership_type, customer_membership.membership.type, membership_name, customer_membership.membership.name, membership_start_date, customer_membership.start_date, membership_expiration_date, customer_membership.expiration_date, membership_allowed_cancellation_date, customer_membership.allowed_cancellation_date, previous_expiration_date, previous_allowed_cancellation_date, other_active_customer_memberships, days_to_add]
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "customers": [    0  ],  "memberships": [    0  ],  "membership_types": [    "pack"  ],  "created_at_lte": "2024-07-29",  "created_at_gte": "2024-07-29",  "updated_at_lte": "2024-07-29",  "updated_at_gte": "2024-07-29",  "created_at_timeframe": "string",  "start_date_lte": "2024-07-29",  "start_date_gte": "2024-07-29",  "start_timeframe": "string",  "end_date_lte": "2024-07-29",  "end_date_gte": "2024-07-29",  "end_timeframe": "string",  "status": [    "active"  ],  "payment_resolution_type": [    "charge"  ],  "is_usage_prorated": True,  "columns": [    "id"  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/customer_membership_holds/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "customers": [    0  ],  "memberships": [    0  ],  "membership_types": [    "pack"  ],  "created_at_lte": "2024-07-29",  "created_at_gte": "2024-07-29",  "updated_at_lte": "2024-07-29",  "updated_at_gte": "2024-07-29",  "created_at_timeframe": "string",  "start_date_lte": "2024-07-29",  "start_date_gte": "2024-07-29",  "start_timeframe": "string",  "end_date_lte": "2024-07-29",  "end_date_gte": "2024-07-29",  "end_timeframe": "string",  "status": [    "active"  ],  "payment_resolution_type": [    "charge"  ],  "is_usage_prorated": True,  "columns": [    "id"  ]}
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
"customers": [
0
],
"memberships": [
0
],
"membership_types": [
"pack"
],
"created_at_lte": "2024-07-29",
"created_at_gte": "2024-07-29",
"updated_at_lte": "2024-07-29",
"updated_at_gte": "2024-07-29",
"created_at_timeframe": "string",
"start_date_lte": "2024-07-29",
"start_date_gte": "2024-07-29",
"start_timeframe": "string",
"end_date_lte": "2024-07-29",
"end_date_gte": "2024-07-29",
"end_timeframe": "string",
"status": [
"active"
],
"payment_resolution_type": [
"charge"
],
"is_usage_prorated": true,
"columns": [
"id"
]
}
```


