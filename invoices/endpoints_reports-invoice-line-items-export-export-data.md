# Endpoints_Reports Invoice Line Items Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/invoice_line_items/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/invoice_line_items/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, invoice_id, invoice.id, invoice, due_date, invoice.due_date, invoice_number, invoice.number, invoice_confirmed_at, invoice.confirmed_at, paid_at, invoice.paid_at, invoice_updated_at, invoice.updated_at, invoice_status, invoice.status, invoice_is_credit_note, invoice.is_credit_note, discount_code_name, invoice.discount_code.name, invoice.discount_code, discount_code, invoice.discount_code.code, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, amount, type, billed_item, description, tax_amount, discount_amount, credit_amount, refund_amount]invoice_statusstringinvoice_due_date_gtestring&lt;date&gt;invoice_due_date_ltestring&lt;date&gt;invoice_paid_at_gtestring&lt;date-time&gt;invoice_paid_at_ltestring&lt;date-time&gt;invoice_updated_at_gtestring&lt;date-time&gt;invoice_updated_at_ltestring&lt;date-time&gt;invoice_confirmed_at_gtestring&lt;date-time&gt;invoice_confirmed_at_ltestring&lt;date-time&gt;Bodyid_gtintegersortstring[]Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, invoice_id, invoice.id, invoice, due_date, invoice.due_date, invoice_number, invoice.number, invoice_confirmed_at, invoice.confirmed_at, paid_at, invoice.paid_at, invoice_updated_at, invoice.updated_at, invoice_status, invoice.status, invoice_is_credit_note, invoice.is_credit_note, discount_code_name, invoice.discount_code.name, invoice.discount_code, discount_code, invoice.discount_code.code, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, amount, type, billed_item, description, tax_amount, discount_amount, credit_amount, refund_amount]invoice_statusstringinvoice_due_date_gtestring&lt;date&gt;invoice_due_date_ltestring&lt;date&gt;invoice_paid_at_gtestring&lt;date-time&gt;invoice_paid_at_ltestring&lt;date-time&gt;invoice_updated_at_gtestring&lt;date-time&gt;invoice_updated_at_ltestring&lt;date-time&gt;invoice_confirmed_at_gtestring&lt;date-time&gt;invoice_confirmed_at_ltestring&lt;date-time&gt;Bodyid_gtintegersortstring[]Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, invoice_id, invoice.id, invoice, due_date, invoice.due_date, invoice_number, invoice.number, invoice_confirmed_at, invoice.confirmed_at, paid_at, invoice.paid_at, invoice_updated_at, invoice.updated_at, invoice_status, invoice.status, invoice_is_credit_note, invoice.is_credit_note, discount_code_name, invoice.discount_code.name, invoice.discount_code, discount_code, invoice.discount_code.code, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, amount, type, billed_item, description, tax_amount, discount_amount, credit_amount, refund_amount]invoice_statusstringinvoice_due_date_gtestring&lt;date&gt;invoice_due_date_ltestring&lt;date&gt;invoice_paid_at_gtestring&lt;date-time&gt;invoice_paid_at_ltestring&lt;date-time&gt;invoice_updated_at_gtestring&lt;date-time&gt;invoice_updated_at_ltestring&lt;date-time&gt;invoice_confirmed_at_gtestring&lt;date-time&gt;invoice_confirmed_at_ltestring&lt;date-time&gt;
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "invoice_status": "string",  "invoice_due_date_gte": "2024-07-29",  "invoice_due_date_lte": "2024-07-29",  "invoice_paid_at_gte": "2024-07-29T15:51:28.071Z",  "invoice_paid_at_lte": "2024-07-29T15:51:28.071Z",  "invoice_updated_at_gte": "2024-07-29T15:51:28.071Z",  "invoice_updated_at_lte": "2024-07-29T15:51:28.071Z",  "invoice_confirmed_at_gte": "2024-07-29T15:51:28.071Z",  "invoice_confirmed_at_lte": "2024-07-29T15:51:28.071Z"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/invoice_line_items/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "invoice_status": "string",  "invoice_due_date_gte": "2024-07-29",  "invoice_due_date_lte": "2024-07-29",  "invoice_paid_at_gte": "2024-07-29T15:51:28.071Z",  "invoice_paid_at_lte": "2024-07-29T15:51:28.071Z",  "invoice_updated_at_gte": "2024-07-29T15:51:28.071Z",  "invoice_updated_at_lte": "2024-07-29T15:51:28.071Z",  "invoice_confirmed_at_gte": "2024-07-29T15:51:28.071Z",  "invoice_confirmed_at_lte": "2024-07-29T15:51:28.071Z"}
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
"id"
],
"invoice_status": "string",
"invoice_due_date_gte": "2024-07-29",
"invoice_due_date_lte": "2024-07-29",
"invoice_paid_at_gte": "2024-07-29T15:51:28.071Z",
"invoice_paid_at_lte": "2024-07-29T15:51:28.071Z",
"invoice_updated_at_gte": "2024-07-29T15:51:28.071Z",
"invoice_updated_at_lte": "2024-07-29T15:51:28.071Z",
"invoice_confirmed_at_gte": "2024-07-29T15:51:28.071Z",
"invoice_confirmed_at_lte": "2024-07-29T15:51:28.071Z"
}
```


