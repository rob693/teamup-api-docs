# Endpoints_Reports Invoice Line Items Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/invoice_line_items`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/invoice_line_items.grouped/data
Query Parameterscolumns string[]Possible values: [total_amount, type]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinvoice_confirmed_at_gte date-timeinvoice_confirmed_at_lte date-timeinvoice_due_date_gte dateinvoice_due_date_lte dateinvoice_paid_at_gte date-timeinvoice_paid_at_lte date-timeinvoice_status stringinvoice_updated_at_gte date-timeinvoice_updated_at_lte date-timelimit integerDefault value: 50offset integerDefault value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-empty
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [total_amount objectThe summed amount/price of the line item.decimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]typestringThe purchase type of the line item.Possible values: [pack_membership, prepaid_plan_membership, recurring_plan_membership, membership_purchase, event_registration, course, course_session, store_order, flat_fee, service_fee]]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "total_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "type": "pack_membership"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/invoice_line_items.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscolumns — querytotal_amounttypeformat — query---csvjsonid_gt — queryinvoice_confirmed_at_gte — queryinvoice_confirmed_at_lte — queryinvoice_due_date_gte — queryinvoice_due_date_lte — queryinvoice_paid_at_gte — queryinvoice_paid_at_lte — queryinvoice_status — queryinvoice_updated_at_gte — queryinvoice_updated_at_lte — querylimit — queryoffset — querypage — querypage_size — querysort — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousInvoice Line Items ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "total_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


