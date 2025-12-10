# Endpoints_Reports Content Views Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/content_views`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/content_views.grouped/data
Query Parameterscolumns string[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, content_id, content.id, content, content_name, content.name, month, year, count], &gt;= 1content integer[]customers integer[]format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerPossible values: &lt;= 100Default value: 50offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.viewed_at_gte date-timeviewed_at_lte date-timeviewed_at_timeframe string
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe unique identifier for the customer who viewed the content.namestringThe full name of the customer who viewed the content.emailstringThe email address of the customer who viewed the content.content objectidintegerThe unique identifier for the content that was viewed.namestringThe name of the content that was viewed.monthintegerCan be used for data groups. The month when the bucketized content was viewed.yearintegerCan be used for data groups. The year when the bucketized content was viewed.countintegerGrouping aggregate. The number of content views for the bucketized content.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "content": {        "id": 0,        "name": "string"      },      "month": 0,      "year": 0,      "count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/content_views.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredcustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailcontent_idcontent.idcontentcontent_namecontent.namemonthyearcountShow optional parameterscontent — queryAdd itemcustomers — queryAdd itemformat — query---csvjsonid_gt — querylimit — queryoffset — querypage — querypage_size — querysort — queryAdd itemviewed_at_gte — queryviewed_at_lte — queryviewed_at_timeframe — querySend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousContent Views ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
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


