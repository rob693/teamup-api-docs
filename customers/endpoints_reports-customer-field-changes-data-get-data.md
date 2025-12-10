# Endpoints_Reports Customer Field Changes Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/customer_field_changes/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/customer_field_changes/data
Query Parameterschanged_at_gte date-timechanged_at_lte date-timechanged_at_timeframe stringcolumns string[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, field_id, field.id, field, field_label, field.label, changed_at, previous_value, new_value]customer_fields integer[]customers integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerPossible values: &lt;= 100Default value: 50offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.field objectidintegerThe unique identifier for the field.labelstringThe label of the field that was changed.changed_atstring&lt;date-time&gt;When the field value was changed.previous_valuestringThe previous value of the field before the change.new_valuestringThe new value of the field after the change.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "field": {        "id": 0,        "label": "string"      },      "changed_at": "2024-07-29T15:51:28.071Z",      "previous_value": "string",      "new_value": "string"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/customer_field_changes/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterschanged_at_gte — querychanged_at_lte — querychanged_at_timeframe — querycolumns — querycustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailfield_idfield.idfieldfield_labelfield.labelchanged_atprevious_valuenew_valuecustomer_fields — queryAdd itemcustomers — queryAdd itemformat — query---csvjsonid_gt — querylimit — queryoffset — querypage — querypage_size — querysort — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCustomer Field Changes ReportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "id": 0,        "label": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


