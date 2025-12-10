# Endpoints_Reports Content Views Grouped Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/content_views`

## Summary
Grouped Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/content_views.grouped/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, content_id, content.id, content, content_name, content.name, month, year, count], &gt;= 1contentinteger[]customersinteger[]viewed_at_ltestring&lt;date-time&gt;viewed_at_gtestring&lt;date-time&gt;viewed_at_timeframestringBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, content_id, content.id, content, content_name, content.name, month, year, count], &gt;= 1contentinteger[]customersinteger[]viewed_at_ltestring&lt;date-time&gt;viewed_at_gtestring&lt;date-time&gt;viewed_at_timeframestringBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, content_id, content.id, content, content_name, content.name, month, year, count], &gt;= 1contentinteger[]customersinteger[]viewed_at_ltestring&lt;date-time&gt;viewed_at_gtestring&lt;date-time&gt;viewed_at_timeframestring
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "content": [    0  ],  "customers": [    0  ],  "viewed_at_lte": "2024-07-29T15:51:28.071Z",  "viewed_at_gte": "2024-07-29T15:51:28.071Z",  "viewed_at_timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/content_views.grouped/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "content": [    0  ],  "customers": [    0  ],  "viewed_at_lte": "2024-07-29T15:51:28.071Z",  "viewed_at_gte": "2024-07-29T15:51:28.071Z",  "viewed_at_timeframe": "string"}
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
"content": [
0
],
"customers": [
0
],
"viewed_at_lte": "2024-07-29T15:51:28.071Z",
"viewed_at_gte": "2024-07-29T15:51:28.071Z",
"viewed_at_timeframe": "string"
}
```


