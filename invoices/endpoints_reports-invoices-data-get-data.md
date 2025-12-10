# Endpoints_Reports Invoices Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/invoices/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/invoices/data
Query Parameterscolumns string[]Possible values: [id, due_date, confirmed_at, paid_at, status, is_credit_note, refunded_invoice_id, refunded_invoice.id, refunded_invoice, number, customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, customer_venue_id, customer.venue.id, customer.venue, customer_venue_name, customer.venue.name, total_amount, subtotal_amount, discount_amount, tax_amount, credit_amount, adjustment_amount, expected_payment_amount, refund_amount, refund_date, discount_code_name, discount_code.name, discount_code, discount_code.code, payment_processor, purchase_type, purchase_items, payout, applied_credits, charges, updated_at, legacy_mapping]confirmed_at_gte date-timeconfirmed_at_lte date-timecredit_applied booleancustomer_memberships integer[]customers integer[]discount_applied booleandue_date_gte datedue_date_lte datedue_date_timeframe stringformat stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerDefault value: 50offset integerDefault value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.paid_at_gte date-timepaid_at_lte date-timepaid_at_timeframe stringpayment_processors integer[]purchase_types string[]Possible values: [class, course, course_session, membership, store]sort string[]Possible values: non-emptystatus stringupdated_at_gte date-timeupdated_at_lte date-time
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [idintegerThe unique identifier for the invoice.due_datestring&lt;date&gt;The date when the invoice is due for payment.confirmed_atstring&lt;date-time&gt;When the invoice was confirmed.paid_atstring&lt;date-time&gt;When the invoice was paid.statusstringThe current status of the invoice.Possible values: [open, paid, pending_offline, pending_online, failed, voided, upcoming, skipped, retrying, retry_failed]is_credit_notebooleanWhether the invoice is a credit note.refunded_invoice objectidintegerThe ID of the invoice that this credit note refunds.numberstringThe provider-assigned invoice number.customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.venue objectidintegerThe unique identifier for the customer's venue.namestringThe name of the customer's venue.total_amount objectThe total amount of the invoice including taxes and discounts.decimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]subtotal_amount objectThe subtotal amount of the invoice before taxes and discounts.decimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]discount_amount objectThe total discount amount applied to the invoice.decimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]tax_amount objectdecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]credit_amount objectdecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]adjustment_amount objectdecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]expected_payment_amount objectdecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]refund_amount objectdecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]refund_datestring&lt;date&gt;discount_code objectnamestringcodestringpayment_processorstringpurchase_typestringpurchase_itemsstringpayoutstringapplied_credits object[]List of credits applied to the invoice.Array [amount objectdecimalstring]charges object[]List of charges associated with the invoice.Array [created_atstring&lt;date-time&gt;amount objectdecimalstringcurrencystringconfirmed_atstring&lt;date-time&gt;]updated_atstring&lt;date-time&gt;When the invoice was last updated.legacy_mappingobjectLegacy system mapping information for the invoice.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "id": 0,      "due_date": "2024-07-29",      "confirmed_at": "2024-07-29T15:51:28.071Z",      "paid_at": "2024-07-29T15:51:28.071Z",      "status": "open",      "is_credit_note": true,      "refunded_invoice": {        "id": 0      },      "number": "string",      "customer": {        "id": 0,        "name": "string",        "email": "string",        "venue": {          "id": 0,          "name": "string"        }      },      "total_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "subtotal_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "discount_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "tax_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "credit_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "adjustment_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "expected_payment_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "refund_amount": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "refund_date": "2024-07-29",      "discount_code": {        "name": "string",        "code": "string"      },      "payment_processor": "string",      "purchase_type": "string",      "purchase_items": "string",      "payout": "string",      "applied_credits": [        {          "amount": {            "decimal": "string"          }        }      ],      "charges": [        {          "created_at": "2024-07-29T15:51:28.071Z",          "amount": {            "decimal": "string",            "currency": "string"          },          "confirmed_at": "2024-07-29T15:51:28.071Z"        }      ],      "updated_at": "2024-07-29T15:51:28.071Z",      "legacy_mapping": {}    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/invoices/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscolumns — queryiddue_dateconfirmed_atpaid_atstatusis_credit_noterefunded_invoice_idrefunded_invoice.idrefunded_invoicenumbercustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailcustomer_venue_idcustomer.venue.idcustomer.venuecustomer_venue_namecustomer.venue.nametotal_amountsubtotal_amountdiscount_amounttax_amountcredit_amountadjustment_amountexpected_payment_amountrefund_amountrefund_datediscount_code_namediscount_code.namediscount_codediscount_code.codepayment_processorpurchase_typepurchase_itemspayoutapplied_creditschargesupdated_atlegacy_mappingconfirmed_at_gte — queryconfirmed_at_lte — querycredit_applied — query---truefalsecustomer_memberships — queryAdd itemcustomers — queryAdd itemdiscount_applied — query---truefalsedue_date_gte — querydue_date_lte — querydue_date_timeframe — queryformat — query---csvjsonid_gt — querylimit — queryoffset — querypage — querypage_size — querypaid_at_gte — querypaid_at_lte — querypaid_at_timeframe — querypayment_processors — queryAdd itempurchase_types — queryclasscoursecourse_sessionmembershipstoresort — queryAdd itemstatus — queryupdated_at_gte — queryupdated_at_lte — querySend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousGrouped Data ExportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "id": 0,      "due_date": "2024-07-29",      "confirmed_at": "2024-07-29T15:51:28.071Z",      "paid_at": "2024-07-29T15:51:28.071Z",      "status": "open",      "is_credit_note": true,      "refunded_invoice": {        "id": 0      }
```

```json
{        "id": 0,        "name": "string",        "email": "string",        "venue": {          "id": 0,          "name": "string"        }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "name": "string",        "code": "string"      }
```

```json
{          "amount": {            "decimal": "string"          }
```

```json
{          "created_at": "2024-07-29T15:51:28.071Z",          "amount": {            "decimal": "string",            "currency": "string"          }
```

```json
{}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


