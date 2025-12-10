# Endpoints_Reports Sms Messages Grouped Data Get Data

**Method:** GET
**URL:** `/api/v2//reports/sms_messages`

## Summary
Grouped Data | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//reports/sms_messages.grouped/data
Query Parameterscolumns string[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, interaction_trigger, interaction.trigger, interaction, count], &gt;= 1customers integer[]Only include rows for particular customers. Formas as customer id values.format stringPossible values: non-empty, [csv, json]
Default value: csvid_gt integerinteraction_triggers string[]Possible values: [waitlist_added, waitlist_spot_available, waitlist_spot_expired, waitlist_removed, event_cancelled, event_changed, event_registration_confirmed, event_reminder, verification_code, two_factor_authentication, broadcast_message, boxmate_journey]Only include rows with particular triggers.limit integerPossible values: &lt;= 100Default value: 50offset integerPossible values: &gt;= 0Default value: 0page integerPossible values: &gt;= 1Specify the page of results to return.page_size integerPossible values: &gt;= 0 and &lt;= 100Specify the number of results to return.sort string[]Possible values: non-emptyThe column names to order the returned rows by. Prefix with a - (minus) sign for descending order.status string[]Possible values: [queued, sent, external_error, delivered, failed, undelivered]Only include rows with particular statuses.status_updated_at_gte date-timeOnly include messages with a status update on or after a timestamp.status_updated_at_lte date-timeOnly include messages with a status update on or before a timestamp.status_updated_at_timeframe stringOnly include messages with a status update within a particular timeframe.
Responses​200OKapplication/jsonSchemaExample (auto)SchematotalintegerThe total number of rows that exist for this report.column_headers object[]A list of objects that describes the data contained in each of the report's columns.Array [labelstringrequiredThe column's display name.Example: Customer IDkeystringrequiredThe property name that keys the column's values in the report rows. If the key is nested, it will use dot-notation.Example: customer.idsortablebooleanrequiredWhether the report rows can be sorted on this column.holds_customer_idbooleanWhether the column holds a customer's unique identifier.sorted objectIf the report is currently sorted on this column, an object that contains information about the sort. Otherwise, this object does not exist.orderstringrequiredWhether this column's values are sorted in descending or ascending order.Possible values: [desc, asc]prioritynumberIf the report is sorted by multiple columns, the priority that this column's values take in determining the order.requiredbooleanWhether this column must always be present in the report response.]rows undefined[]Array [customer objectidintegerThe customer's unique identifier.namestringThe customer's name.emailstringThe customer's email.statusstringThe message status.Possible values: [queued, sent, external_error, delivered, failed, undelivered]interaction objecttriggerstringThe event type that triggered the message.Possible values: [waitlist_added, waitlist_spot_available, waitlist_spot_expired, waitlist_removed, event_cancelled, event_changed, event_registration_confirmed, event_reminder, verification_code, two_factor_authentication, broadcast_message, boxmate_journey]countintegerThe total number of SMS messages in the group.]{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      },      "required": true    }  ],  "rows": [    {      "customer": {        "id": 0,        "name": "string",        "email": "string"      },      "status": "queued",      "interaction": {        "trigger": "waitlist_added"      },      "count": 0    }  ]}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/reports/sms_messages.grouped/data", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParameterscolumns — queryrequiredcustomer_idcustomer.idcustomercustomer_namecustomer.namecustomer_emailcustomer.emailstatusinteraction_triggerinteraction.triggerinteractioncountShow optional parameterscustomers — queryAdd itemformat — query---csvjsonid_gt — queryinteraction_triggers — querywaitlist_addedwaitlist_spot_availablewaitlist_spot_expiredwaitlist_removedevent_cancelledevent_changedevent_registration_confirmedevent_reminderverification_codetwo_factor_authenticationbroadcast_messageboxmate_journeylimit — queryoffset — querypage — querypage_size — querysort — queryAdd itemstatus — queryqueuedsentexternal_errordeliveredfailedundeliveredstatus_updated_at_gte — querystatus_updated_at_lte — querystatus_updated_at_timeframe — querySend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousSMS Messages ReportNextGrouped Data ExportCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "total": 0,  "column_headers": [    {      "label": "Customer ID",      "key": "customer.id",      "sortable": true,      "holds_customer_id": true,      "sorted": {        "order": "desc",        "priority": 0      }
```

```json
{      "customer": {        "id": 0,        "name": "string",        "email": "string"      }
```

```json
{        "trigger": "waitlist_added"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


