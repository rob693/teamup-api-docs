# Endpoints_Reports Discount Code Uses Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/discount_code_uses/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/discount_code_uses/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, discount_code_id, discount_code.id, discount_code, discount_code_name, discount_code.name, discount_code_code, discount_code.code, group_id, group.id, group, group_name, group.name, use_type, used_for, used_at]discount_codesinteger[]customersinteger[]groupsinteger[]use_typesstring[]Possible values: [class, course, membership, store_order]used_at_ltestring&lt;date-time&gt;used_at_gtestring&lt;date-time&gt;used_at_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, discount_code_id, discount_code.id, discount_code, discount_code_name, discount_code.name, discount_code_code, discount_code.code, group_id, group.id, group, group_name, group.name, use_type, used_for, used_at]discount_codesinteger[]customersinteger[]groupsinteger[]use_typesstring[]Possible values: [class, course, membership, store_order]used_at_ltestring&lt;date-time&gt;used_at_gtestring&lt;date-time&gt;used_at_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, discount_code_id, discount_code.id, discount_code, discount_code_name, discount_code.name, discount_code_code, discount_code.code, group_id, group.id, group, group_name, group.name, use_type, used_for, used_at]discount_codesinteger[]customersinteger[]groupsinteger[]use_typesstring[]Possible values: [class, course, membership, store_order]used_at_ltestring&lt;date-time&gt;used_at_gtestring&lt;date-time&gt;used_at_timeframestring
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "discount_codes": [    0  ],  "customers": [    0  ],  "groups": [    0  ],  "use_types": [    "class"  ],  "used_at_lte": "2024-07-29T15:51:28.071Z",  "used_at_gte": "2024-07-29T15:51:28.071Z",  "used_at_timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/discount_code_uses/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "discount_codes": [    0  ],  "customers": [    0  ],  "groups": [    0  ],  "use_types": [    "class"  ],  "used_at_lte": "2024-07-29T15:51:28.071Z",  "used_at_gte": "2024-07-29T15:51:28.071Z",  "used_at_timeframe": "string"}
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
"columns": [
"customer_id"
],
"discount_codes": [
0
],
"customers": [
0
],
"groups": [
0
],
"use_types": [
"class"
],
"used_at_lte": "2024-07-29T15:51:28.071Z",
"used_at_gte": "2024-07-29T15:51:28.071Z",
"used_at_timeframe": "string"
}
```


