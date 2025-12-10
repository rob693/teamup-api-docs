# Endpoints_Reports Waiver Signatures Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/waiver_signatures/data`

## Summary
Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/waiver_signatures/data
Query Parameterscolumns string[]Possible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, waiver_id, waiver.id, waiver, waiver_name, waiver.name, signed_at, download_url]customers integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerPossible values: &lt;= 100Default value: 50offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.signed_at_gte date-timesigned_at_lte date-timesigned_at_timeframe stringsort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.waivers integer[]
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer.namestringThe customer's full name.emailstringThe customer's email address.waiver objectidintegerThe unique identifier for the waiver.namestringThe name of the waiver.signed_atstring&lt;date-time&gt;When the waiver was signed.download_urlstringThe download URL for the signed waiver PDF.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "waiver": {        "id": 0,        "name": "string"      },      "signed_at": "2024-07-29T15:51:28.071Z",      "download_url": "string"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/waiver_signatures/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parameterscolumns — querycustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailwaiver_idwaiver.idwaiverwaiver_namewaiver.namesigned_atdownload_urlcustomers — queryAdd itemformat — query---csvjsonid_gt — querylimit — queryoffset — querypage — querypage_size — querysigned_at_gte — querysigned_at_lte — querysigned_at_timeframe — querysort — queryAdd itemwaivers — queryAdd itemSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousWaiver Signatures ReportNextData ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "id": 0,        "name": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


