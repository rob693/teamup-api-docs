# Endpoints_Reports Customer Memberships Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/customer_memberships/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/customer_memberships/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvidsinteger[]customersinteger[]membershipsinteger[]membership_categoriesinteger[]payment_processorsstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$has_expiration_datebooleanhas_active_holdbooleanhas_custom_limitsbooleanis_first_membershipbooleanstart_date_ltestring&lt;date&gt;start_date_gtestring&lt;date&gt;start_date_timeframestringexpiration_date_ltestring&lt;date&gt;expiration_date_gtestring&lt;date&gt;expiration_date_timeframestringrenewal_date_ltestring&lt;date&gt;renewal_date_gtestring&lt;date&gt;renewal_date_timeframestringdowngrade_date_ltestring&lt;date&gt;downgrade_date_gtestring&lt;date&gt;downgrade_date_timeframestringupgrade_date_ltestring&lt;date&gt;upgrade_date_gtestring&lt;date&gt;upgrade_date_timeframestringactive_hold_start_date_ltestring&lt;date&gt;active_hold_start_date_gtestring&lt;date&gt;active_hold_end_date_ltestring&lt;date&gt;active_hold_end_date_gtestring&lt;date&gt;purchased_at_ltestring&lt;date-time&gt;purchased_at_gtestring&lt;date-time&gt;purchased_at_timeframestringcancelled_at_ltestring&lt;date-time&gt;cancelled_at_gtestring&lt;date-time&gt;cancelled_at_timeframestringupdated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;statusstring[]Possible values: [active, hold, cancelled, completed, upgraded, downgraded]typesstring[]Possible values: [pack, prepaid, recurring]columnsstring[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, other_active, membership_id, membership.id, membership, membership_name, membership.name, type, status, payment_processor, purchase_date, start_date, expiration_date, renewal_date, cancelled_date, downgraded_date, upgraded_date, has_custom_limits, is_first_membership, billed_price, cancellation_reason, completed_at]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvidsinteger[]customersinteger[]membershipsinteger[]membership_categoriesinteger[]payment_processorsstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$has_expiration_datebooleanhas_active_holdbooleanhas_custom_limitsbooleanis_first_membershipbooleanstart_date_ltestring&lt;date&gt;start_date_gtestring&lt;date&gt;start_date_timeframestringexpiration_date_ltestring&lt;date&gt;expiration_date_gtestring&lt;date&gt;expiration_date_timeframestringrenewal_date_ltestring&lt;date&gt;renewal_date_gtestring&lt;date&gt;renewal_date_timeframestringdowngrade_date_ltestring&lt;date&gt;downgrade_date_gtestring&lt;date&gt;downgrade_date_timeframestringupgrade_date_ltestring&lt;date&gt;upgrade_date_gtestring&lt;date&gt;upgrade_date_timeframestringactive_hold_start_date_ltestring&lt;date&gt;active_hold_start_date_gtestring&lt;date&gt;active_hold_end_date_ltestring&lt;date&gt;active_hold_end_date_gtestring&lt;date&gt;purchased_at_ltestring&lt;date-time&gt;purchased_at_gtestring&lt;date-time&gt;purchased_at_timeframestringcancelled_at_ltestring&lt;date-time&gt;cancelled_at_gtestring&lt;date-time&gt;cancelled_at_timeframestringupdated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;statusstring[]Possible values: [active, hold, cancelled, completed, upgraded, downgraded]typesstring[]Possible values: [pack, prepaid, recurring]columnsstring[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, other_active, membership_id, membership.id, membership, membership_name, membership.name, type, status, payment_processor, purchase_date, start_date, expiration_date, renewal_date, cancelled_date, downgraded_date, upgraded_date, has_custom_limits, is_first_membership, billed_price, cancellation_reason, completed_at]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvidsinteger[]customersinteger[]membershipsinteger[]membership_categoriesinteger[]payment_processorsstring[]Possible values: non-empty, Value must match regular expression ^(\d+|none)$has_expiration_datebooleanhas_active_holdbooleanhas_custom_limitsbooleanis_first_membershipbooleanstart_date_ltestring&lt;date&gt;start_date_gtestring&lt;date&gt;start_date_timeframestringexpiration_date_ltestring&lt;date&gt;expiration_date_gtestring&lt;date&gt;expiration_date_timeframestringrenewal_date_ltestring&lt;date&gt;renewal_date_gtestring&lt;date&gt;renewal_date_timeframestringdowngrade_date_ltestring&lt;date&gt;downgrade_date_gtestring&lt;date&gt;downgrade_date_timeframestringupgrade_date_ltestring&lt;date&gt;upgrade_date_gtestring&lt;date&gt;upgrade_date_timeframestringactive_hold_start_date_ltestring&lt;date&gt;active_hold_start_date_gtestring&lt;date&gt;active_hold_end_date_ltestring&lt;date&gt;active_hold_end_date_gtestring&lt;date&gt;purchased_at_ltestring&lt;date-time&gt;purchased_at_gtestring&lt;date-time&gt;purchased_at_timeframestringcancelled_at_ltestring&lt;date-time&gt;cancelled_at_gtestring&lt;date-time&gt;cancelled_at_timeframestringupdated_at_ltestring&lt;date-time&gt;updated_at_gtestring&lt;date-time&gt;statusstring[]Possible values: [active, hold, cancelled, completed, upgraded, downgraded]typesstring[]Possible values: [pack, prepaid, recurring]columnsstring[]Possible values: [id, updated_at, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, other_active, membership_id, membership.id, membership, membership_name, membership.name, type, status, payment_processor, purchase_date, start_date, expiration_date, renewal_date, cancelled_date, downgraded_date, upgraded_date, has_custom_limits, is_first_membership, billed_price, cancellation_reason, completed_at]
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "ids": [    0  ],  "customers": [    0  ],  "memberships": [    0  ],  "membership_categories": [    0  ],  "payment_processors": [    "string"  ],  "has_expiration_date": True,  "has_active_hold": True,  "has_custom_limits": True,  "is_first_membership": True,  "start_date_lte": "2024-07-29",  "start_date_gte": "2024-07-29",  "start_date_timeframe": "string",  "expiration_date_lte": "2024-07-29",  "expiration_date_gte": "2024-07-29",  "expiration_date_timeframe": "string",  "renewal_date_lte": "2024-07-29",  "renewal_date_gte": "2024-07-29",  "renewal_date_timeframe": "string",  "downgrade_date_lte": "2024-07-29",  "downgrade_date_gte": "2024-07-29",  "downgrade_date_timeframe": "string",  "upgrade_date_lte": "2024-07-29",  "upgrade_date_gte": "2024-07-29",  "upgrade_date_timeframe": "string",  "active_hold_start_date_lte": "2024-07-29",  "active_hold_start_date_gte": "2024-07-29",  "active_hold_end_date_lte": "2024-07-29",  "active_hold_end_date_gte": "2024-07-29",  "purchased_at_lte": "2024-07-29T15:51:28.071Z",  "purchased_at_gte": "2024-07-29T15:51:28.071Z",  "purchased_at_timeframe": "string",  "cancelled_at_lte": "2024-07-29T15:51:28.071Z",  "cancelled_at_gte": "2024-07-29T15:51:28.071Z",  "cancelled_at_timeframe": "string",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "status": [    "active"  ],  "types": [    "pack"  ],  "columns": [    "id"  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/customer_memberships/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "ids": [    0  ],  "customers": [    0  ],  "memberships": [    0  ],  "membership_categories": [    0  ],  "payment_processors": [    "string"  ],  "has_expiration_date": True,  "has_active_hold": True,  "has_custom_limits": True,  "is_first_membership": True,  "start_date_lte": "2024-07-29",  "start_date_gte": "2024-07-29",  "start_date_timeframe": "string",  "expiration_date_lte": "2024-07-29",  "expiration_date_gte": "2024-07-29",  "expiration_date_timeframe": "string",  "renewal_date_lte": "2024-07-29",  "renewal_date_gte": "2024-07-29",  "renewal_date_timeframe": "string",  "downgrade_date_lte": "2024-07-29",  "downgrade_date_gte": "2024-07-29",  "downgrade_date_timeframe": "string",  "upgrade_date_lte": "2024-07-29",  "upgrade_date_gte": "2024-07-29",  "upgrade_date_timeframe": "string",  "active_hold_start_date_lte": "2024-07-29",  "active_hold_start_date_gte": "2024-07-29",  "active_hold_end_date_lte": "2024-07-29",  "active_hold_end_date_gte": "2024-07-29",  "purchased_at_lte": "2024-07-29T15:51:28.071Z",  "purchased_at_gte": "2024-07-29T15:51:28.071Z",  "purchased_at_timeframe": "string",  "cancelled_at_lte": "2024-07-29T15:51:28.071Z",  "cancelled_at_gte": "2024-07-29T15:51:28.071Z",  "cancelled_at_timeframe": "string",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "status": [    "active"  ],  "types": [    "pack"  ],  "columns": [    "id"  ]}
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
"ids": [
0
],
"customers": [
0
],
"memberships": [
0
],
"membership_categories": [
0
],
"payment_processors": [
"string"
],
"has_expiration_date": true,
"has_active_hold": true,
"has_custom_limits": true,
"is_first_membership": true,
"start_date_lte": "2024-07-29",
"start_date_gte": "2024-07-29",
"start_date_timeframe": "string",
"expiration_date_lte": "2024-07-29",
"expiration_date_gte": "2024-07-29",
"expiration_date_timeframe": "string",
"renewal_date_lte": "2024-07-29",
"renewal_date_gte": "2024-07-29",
"renewal_date_timeframe": "string",
"downgrade_date_lte": "2024-07-29",
"downgrade_date_gte": "2024-07-29",
"downgrade_date_timeframe": "string",
"upgrade_date_lte": "2024-07-29",
"upgrade_date_gte": "2024-07-29",
"upgrade_date_timeframe": "string",
"active_hold_start_date_lte": "2024-07-29",
"active_hold_start_date_gte": "2024-07-29",
"active_hold_end_date_lte": "2024-07-29",
"active_hold_end_date_gte": "2024-07-29",
"purchased_at_lte": "2024-07-29T15:51:28.071Z",
"purchased_at_gte": "2024-07-29T15:51:28.071Z",
"purchased_at_timeframe": "string",
"cancelled_at_lte": "2024-07-29T15:51:28.071Z",
"cancelled_at_gte": "2024-07-29T15:51:28.071Z",
"cancelled_at_timeframe": "string",
"updated_at_lte": "2024-07-29T15:51:28.071Z",
"updated_at_gte": "2024-07-29T15:51:28.071Z",
"status": [
"active"
],
"types": [
"pack"
],
"columns": [
"id"
]
}
```


