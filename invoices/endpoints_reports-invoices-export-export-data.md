# Endpoints_Reports Invoices Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/invoices/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/invoices/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, due_date, confirmed_at, paid_at, status, is_credit_note, refunded_invoice_id, refunded_invoice.id, refunded_invoice, number, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, total_amount, subtotal_amount, discount_amount, tax_amount, credit_amount, adjustment_amount, expected_payment_amount, refund_amount, refund_date, discount_code_name, discount_code.name, discount_code, discount_code.code, payment_processor, purchase_type, purchase_items, payout, applied_credits, charges, updated_at, legacy_mapping]customersinteger[]payment_processorsinteger[]purchase_typesstring[]Possible values: [class, course, course_session, membership, store]statusstringdue_date_gtestring&lt;date&gt;due_date_ltestring&lt;date&gt;due_date_timeframestringupdated_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;confirmed_at_gtestring&lt;date-time&gt;confirmed_at_ltestring&lt;date-time&gt;paid_at_gtestring&lt;date-time&gt;paid_at_ltestring&lt;date-time&gt;paid_at_timeframestringcustomer_membershipsinteger[]discount_appliedbooleancredit_appliedbooleanBodyid_gtintegersortstring[]Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, due_date, confirmed_at, paid_at, status, is_credit_note, refunded_invoice_id, refunded_invoice.id, refunded_invoice, number, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, total_amount, subtotal_amount, discount_amount, tax_amount, credit_amount, adjustment_amount, expected_payment_amount, refund_amount, refund_date, discount_code_name, discount_code.name, discount_code, discount_code.code, payment_processor, purchase_type, purchase_items, payout, applied_credits, charges, updated_at, legacy_mapping]customersinteger[]payment_processorsinteger[]purchase_typesstring[]Possible values: [class, course, course_session, membership, store]statusstringdue_date_gtestring&lt;date&gt;due_date_ltestring&lt;date&gt;due_date_timeframestringupdated_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;confirmed_at_gtestring&lt;date-time&gt;confirmed_at_ltestring&lt;date-time&gt;paid_at_gtestring&lt;date-time&gt;paid_at_ltestring&lt;date-time&gt;paid_at_timeframestringcustomer_membershipsinteger[]discount_appliedbooleancredit_appliedbooleanBodyid_gtintegersortstring[]Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Possible values: [id, due_date, confirmed_at, paid_at, status, is_credit_note, refunded_invoice_id, refunded_invoice.id, refunded_invoice, number, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, total_amount, subtotal_amount, discount_amount, tax_amount, credit_amount, adjustment_amount, expected_payment_amount, refund_amount, refund_date, discount_code_name, discount_code.name, discount_code, discount_code.code, payment_processor, purchase_type, purchase_items, payout, applied_credits, charges, updated_at, legacy_mapping]customersinteger[]payment_processorsinteger[]purchase_typesstring[]Possible values: [class, course, course_session, membership, store]statusstringdue_date_gtestring&lt;date&gt;due_date_ltestring&lt;date&gt;due_date_timeframestringupdated_at_gtestring&lt;date-time&gt;updated_at_ltestring&lt;date-time&gt;confirmed_at_gtestring&lt;date-time&gt;confirmed_at_ltestring&lt;date-time&gt;paid_at_gtestring&lt;date-time&gt;paid_at_ltestring&lt;date-time&gt;paid_at_timeframestringcustomer_membershipsinteger[]discount_appliedbooleancredit_appliedboolean
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "customers": [    0  ],  "payment_processors": [    0  ],  "purchase_types": [    "class"  ],  "status": "string",  "due_date_gte": "2024-07-29",  "due_date_lte": "2024-07-29",  "due_date_timeframe": "string",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "confirmed_at_gte": "2024-07-29T15:51:28.071Z",  "confirmed_at_lte": "2024-07-29T15:51:28.071Z",  "paid_at_gte": "2024-07-29T15:51:28.071Z",  "paid_at_lte": "2024-07-29T15:51:28.071Z",  "paid_at_timeframe": "string",  "customer_memberships": [    0  ],  "discount_applied": True,  "credit_applied": True})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/invoices/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "customers": [    0  ],  "payment_processors": [    0  ],  "purchase_types": [    "class"  ],  "status": "string",  "due_date_gte": "2024-07-29",  "due_date_lte": "2024-07-29",  "due_date_timeframe": "string",  "updated_at_gte": "2024-07-29T15:51:28.071Z",  "updated_at_lte": "2024-07-29T15:51:28.071Z",  "confirmed_at_gte": "2024-07-29T15:51:28.071Z",  "confirmed_at_lte": "2024-07-29T15:51:28.071Z",  "paid_at_gte": "2024-07-29T15:51:28.071Z",  "paid_at_lte": "2024-07-29T15:51:28.071Z",  "paid_at_timeframe": "string",  "customer_memberships": [    0  ],  "discount_applied": True,  "credit_applied": True}
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
"customers": [
0
],
"payment_processors": [
0
],
"purchase_types": [
"class"
],
"status": "string",
"due_date_gte": "2024-07-29",
"due_date_lte": "2024-07-29",
"due_date_timeframe": "string",
"updated_at_gte": "2024-07-29T15:51:28.071Z",
"updated_at_lte": "2024-07-29T15:51:28.071Z",
"confirmed_at_gte": "2024-07-29T15:51:28.071Z",
"confirmed_at_lte": "2024-07-29T15:51:28.071Z",
"paid_at_gte": "2024-07-29T15:51:28.071Z",
"paid_at_lte": "2024-07-29T15:51:28.071Z",
"paid_at_timeframe": "string",
"customer_memberships": [
0
],
"discount_applied": true,
"credit_applied": true
}
```


