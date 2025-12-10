# Endpoints_Reports Discount Code Uses Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/discount_code_uses/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/discount_code_uses/data
Query Parameterscolumns string[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, discount_code_id, discount_code.id, discount_code, discount_code_name, discount_code.name, discount_code_code, discount_code.code, group_id, group.id, group, group_name, group.name, use_type, used_for, used_at]customers integer[]discount_codes integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvgroups integer[]id_gt integerlimit integerPossible values: &lt;= 100Default value: 50offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.use_types string[]Possible values: [class, course, membership, store_order]used_at_gte date-timeused_at_lte date-timeused_at_timeframe string
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer.namestringThe name of the customer.emailstringThe email address of the customer.discount_code objectidintegerThe unique identifier for the discount code.namestringThe name of the discount code.codestringThe code of the discount code.group objectidintegerThe unique identifier for the discount code group.namestringuse_typestringPossible values: [class, course, membership, store_order, unknown]used_for objectidintegerlabelstringtypestringused_atstring&lt;date-time&gt;When the discount code was used.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "discount_code": {        "id": 0,        "name": "string",        "code": "string"      },      "group": {        "id": 0,        "name": "string"      },      "use_type": "class",      "used_for": {        "id": 0,        "label": "string",        "type": "string"      },      "used_at": "2024-07-29T15:51:28.071Z"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/discount_code_uses/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscolumns — querycustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emaildiscount_code_iddiscount_code.iddiscount_codediscount_code_namediscount_code.namediscount_code_codediscount_code.codegroup_idgroup.idgroupgroup_namegroup.nameuse_typeused_forused_atcustomers — queryAdd itemdiscount_codes — queryAdd itemformat — query---csvjsongroups — queryAdd itemid_gt — querylimit — queryoffset — querypage — querypage_size — querysort — queryAdd itemuse_types — queryclasscoursemembershipstore_orderused_at_gte — queryused_at_lte — queryused_at_timeframe — querySend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousGrouped Data ExportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "id": 0,        "name": "string",        "code": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{        "id": 0,        "label": "string",        "type": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


