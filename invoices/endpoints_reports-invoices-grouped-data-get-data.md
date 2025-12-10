# Endpoints_Reports Invoices Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/invoices`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/invoices.grouped/data
Query Parameterscolumns string[]requiredPossible values: [status, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, purchase_type, payment_processor, due_date_month, due_date_year, payment_month, payment_year, payout_month, payout_year, purchased_item, purchase_fee_type, count], &gt;= 1confirmed_at_gte date-timeconfirmed_at_lte date-timecredit_applied booleancustomer_memberships integer[]customers integer[]discount_applied booleandue_date_gte datedue_date_lte datedue_date_timeframe stringformat stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerDefault value: 50offset integerDefault value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.paid_at_gte date-timepaid_at_lte date-timepaid_at_timeframe stringpayment_processors integer[]purchase_types string[]Possible values: [class, course, course_session, membership, store]sort string[]Possible values: non-emptystatus stringupdated_at_gte date-timeupdated_at_lte date-time
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [statusstringThe current status of the invoice.Possible values: [open, paid, pending_offline, pending_online, failed, voided, upcoming, skipped, retrying, retry_failed]customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.purchase_typestringpayment_processorstringThe payment processor used for the invoice.due_date_monthstringdue_date_yearstringpayment_monthintegerThe month when the invoice was paid.payment_yearintegerThe year when the invoice was paid.payout_monthstringpayout_yearstringpurchased_itemobjectThe main item that was purchased on the invoice.purchase_fee_typestringThe type of purchase fee applied to the invoice.countstring]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "status": "open",      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "purchase_type": "string",      "payment_processor": "string",      "due_date_month": "string",      "due_date_year": "string",      "payment_month": 0,      "payment_year": 0,      "payout_month": "string",      "payout_year": "string",      "purchased_item": {},      "purchase_fee_type": "string",      "count": "string"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/invoices.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredstatuscustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailpurchase_typepayment_processordue_date_monthdue_date_yearpayment_monthpayment_yearpayout_monthpayout_yearpurchased_itempurchase_fee_typecountShow optional parametersconfirmed_at_gte — queryconfirmed_at_lte — querycredit_applied — query---truefalsecustomer_memberships — queryAdd itemcustomers — queryAdd itemdiscount_applied — query---truefalsedue_date_gte — querydue_date_lte — querydue_date_timeframe — queryformat — query---csvjsonid_gt — querylimit — queryoffset — querypage — querypage_size — querypaid_at_gte — querypaid_at_lte — querypaid_at_timeframe — querypayment_processors — queryAdd itempurchase_types — queryclasscoursecourse_sessionmembershipstoresort — queryAdd itemstatus — queryupdated_at_gte — queryupdated_at_lte — querySend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousInvoices ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "status": "open",      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


