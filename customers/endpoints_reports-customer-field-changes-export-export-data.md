# Endpoints_Reports Customer Field Changes Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/customer_field_changes/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/customer_field_changes/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcustomersinteger[]customer_fieldsinteger[]changed_at_gtestring&lt;date-time&gt;changed_at_ltestring&lt;date-time&gt;changed_at_timeframestringcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, field_id, field.id, field, field_label, field.label, changed_at, previous_value, new_value]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcustomersinteger[]customer_fieldsinteger[]changed_at_gtestring&lt;date-time&gt;changed_at_ltestring&lt;date-time&gt;changed_at_timeframestringcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, field_id, field.id, field, field_label, field.label, changed_at, previous_value, new_value]Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcustomersinteger[]customer_fieldsinteger[]changed_at_gtestring&lt;date-time&gt;changed_at_ltestring&lt;date-time&gt;changed_at_timeframestringcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, field_id, field.id, field, field_label, field.label, changed_at, previous_value, new_value]
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "customers": [    0  ],  "customer_fields": [    0  ],  "changed_at_gte": "2024-07-29T15:51:28.071Z",  "changed_at_lte": "2024-07-29T15:51:28.071Z",  "changed_at_timeframe": "string",  "columns": [    "customer_id"  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/customer_field_changes/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "customers": [    0  ],  "customer_fields": [    0  ],  "changed_at_gte": "2024-07-29T15:51:28.071Z",  "changed_at_lte": "2024-07-29T15:51:28.071Z",  "changed_at_timeframe": "string",  "columns": [    "customer_id"  ]}
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
"customer_fields": [
0
],
"changed_at_gte": "2024-07-29T15:51:28.071Z",
"changed_at_lte": "2024-07-29T15:51:28.071Z",
"changed_at_timeframe": "string",
"columns": [
"customer_id"
]
}
```


