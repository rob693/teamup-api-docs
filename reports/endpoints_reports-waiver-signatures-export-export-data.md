# Endpoints_Reports Waiver Signatures Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/waiver_signatures/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/waiver_signatures/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, waiver_id, waiver.id, waiver, waiver_name, waiver.name, signed_at, download_url]customersinteger[]waiversinteger[]signed_at_ltestring&lt;date-time&gt;signed_at_gtestring&lt;date-time&gt;signed_at_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, waiver_id, waiver.id, waiver, waiver_name, waiver.name, signed_at, download_url]customersinteger[]waiversinteger[]signed_at_ltestring&lt;date-time&gt;signed_at_gtestring&lt;date-time&gt;signed_at_timeframestringBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, waiver_id, waiver.id, waiver, waiver_name, waiver.name, signed_at, download_url]customersinteger[]waiversinteger[]signed_at_ltestring&lt;date-time&gt;signed_at_gtestring&lt;date-time&gt;signed_at_timeframestring
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "customers": [    0  ],  "waivers": [    0  ],  "signed_at_lte": "2024-07-29T15:51:28.071Z",  "signed_at_gte": "2024-07-29T15:51:28.071Z",  "signed_at_timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/waiver_signatures/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "customers": [    0  ],  "waivers": [    0  ],  "signed_at_lte": "2024-07-29T15:51:28.071Z",  "signed_at_gte": "2024-07-29T15:51:28.071Z",  "signed_at_timeframe": "string"}
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
"customers": [
0
],
"waivers": [
0
],
"signed_at_lte": "2024-07-29T15:51:28.071Z",
"signed_at_gte": "2024-07-29T15:51:28.071Z",
"signed_at_timeframe": "string"
}
```


