# Endpoints_Reports Customer Referrals Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/customer_referrals`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/customer_referrals.grouped/data
Query Parameterscolumns string[]requiredPossible values: [referring_customer_id, referring_customer.id, referring_customer, referrering_customer_name, referring_customer.name, referrering_customer_email, referring_customer.email, membership_id, signup_membership.id, signup_membership, membership_name, signup_membership.name, signup_month, signup_year, status, count]confirmation_date_gte dateconfirmation_date_lte dateconfirmation_date_timeframe Only return rows for referrals that were confirmed within a particular timeframe. See section on timeframe syntax for formatting.format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerlimit integerPossible values: &lt;= 100Default value: 50memberships integer[]offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.referring_customers integer[]signup_customers integer[]signup_date_gte datesignup_date_lte datesignup_date_timeframe Only return rows for referrals with a singup date within a particular timeframe. See section on timeframe syntax for formatting.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [pending, confirmed]updated_at_gte date-timeupdated_at_lte date-time
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [referring_customer objectidintegerThe unique identifier of the customer who made the referral.namestringThe name of the customer who made the referral.emailstringThe email address of the customer who made the referral.signup_membership objectidstringThe unique identifier of the membership that the referred member signed up for.namestringThe name of the membership that the referred member signed up for.signup_monthstringsignup_yearstringstatusstringThe status of the referral.Possible values: [pending, confirmed, cancelled]countstring]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "referring_customer": {        "id": 0,        "name": "string",        "email": "string"      },      "signup_membership": {        "id": "string",        "name": "string"      },      "signup_month": "string",      "signup_year": "string",      "status": "pending",      "count": "string"    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/customer_referrals.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredreferring_customer_idreferring_customer.idreferring_customerreferrering_customer_namereferring_customer.namereferrering_customer_emailreferring_customer.emailmembership_idsignup_membership.idsignup_membershipmembership_namesignup_membership.namesignup_monthsignup_yearstatuscountShow optional parametersconfirmation_date_gte — queryconfirmation_date_lte — queryconfirmation_date_timeframe — queryformat — query---csvjsonid_gt — querylimit — querymemberships — queryAdd itemoffset — querypage — querypage_size — queryreferring_customers — queryAdd itemsignup_customers — queryAdd itemsignup_date_gte — querysignup_date_lte — querysignup_date_timeframe — querysort — queryAdd itemstatus — querypendingconfirmedupdated_at_gte — queryupdated_at_lte — querySend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCustomer Referrals ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "referring_customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "id": "string",        "name": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


