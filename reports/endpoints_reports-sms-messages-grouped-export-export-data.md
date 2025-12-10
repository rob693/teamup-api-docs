# Endpoints_Reports Sms Messages Grouped Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/sms_messages`

## Summary
Grouped Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/sms_messages.grouped/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, interaction_trigger, interaction.trigger, interaction, count], &gt;= 1statusstring[]Only include rows with particular statuses.Possible values: [queued, sent, external_error, delivered, failed, undelivered]interaction_triggersstring[]Only include rows with particular triggers.Possible values: [waitlist_added, waitlist_spot_available, waitlist_spot_expired, waitlist_removed, event_cancelled, event_changed, event_registration_confirmed, event_reminder, verification_code, two_factor_authentication, broadcast_message, boxmate_journey]customersinteger[]Only include rows for particular customers. Formas as customer id values.status_updated_at_ltestring&lt;date-time&gt;Only include messages with a status update on or before a timestamp.status_updated_at_gtestring&lt;date-time&gt;Only include messages with a status update on or after a timestamp.status_updated_at_timeframestringOnly include messages with a status update within a particular timeframe.Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, interaction_trigger, interaction.trigger, interaction, count], &gt;= 1statusstring[]Only include rows with particular statuses.Possible values: [queued, sent, external_error, delivered, failed, undelivered]interaction_triggersstring[]Only include rows with particular triggers.Possible values: [waitlist_added, waitlist_spot_available, waitlist_spot_expired, waitlist_removed, event_cancelled, event_changed, event_registration_confirmed, event_reminder, verification_code, two_factor_authentication, broadcast_message, boxmate_journey]customersinteger[]Only include rows for particular customers. Formas as customer id values.status_updated_at_ltestring&lt;date-time&gt;Only include messages with a status update on or before a timestamp.status_updated_at_gtestring&lt;date-time&gt;Only include messages with a status update on or after a timestamp.status_updated_at_timeframestringOnly include messages with a status update within a particular timeframe.Bodyrequiredid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]requiredPossible values: [customer_id, customer.id, customer, customer_name, customer.name, customer_email, customer.email, status, interaction_trigger, interaction.trigger, interaction, count], &gt;= 1statusstring[]Only include rows with particular statuses.Possible values: [queued, sent, external_error, delivered, failed, undelivered]interaction_triggersstring[]Only include rows with particular triggers.Possible values: [waitlist_added, waitlist_spot_available, waitlist_spot_expired, waitlist_removed, event_cancelled, event_changed, event_registration_confirmed, event_reminder, verification_code, two_factor_authentication, broadcast_message, boxmate_journey]customersinteger[]Only include rows for particular customers. Formas as customer id values.status_updated_at_ltestring&lt;date-time&gt;Only include messages with a status update on or before a timestamp.status_updated_at_gtestring&lt;date-time&gt;Only include messages with a status update on or after a timestamp.status_updated_at_timeframestringOnly include messages with a status update within a particular timeframe.
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "status": [    "queued"  ],  "interaction_triggers": [    "waitlist_added"  ],  "customers": [    0  ],  "status_updated_at_lte": "2024-07-29T15:51:28.071Z",  "status_updated_at_gte": "2024-07-29T15:51:28.071Z",  "status_updated_at_timeframe": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/sms_messages.grouped/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
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
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "customer_id"  ],  "status": [    "queued"  ],  "interaction_triggers": [    "waitlist_added"  ],  "customers": [    0  ],  "status_updated_at_lte": "2024-07-29T15:51:28.071Z",  "status_updated_at_gte": "2024-07-29T15:51:28.071Z",  "status_updated_at_timeframe": "string"}
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
"customer_id"
],
"status": [
"queued"
],
"interaction_triggers": [
"waitlist_added"
],
"customers": [
0
],
"status_updated_at_lte": "2024-07-29T15:51:28.071Z",
"status_updated_at_gte": "2024-07-29T15:51:28.071Z",
"status_updated_at_timeframe": "string"
}
```


