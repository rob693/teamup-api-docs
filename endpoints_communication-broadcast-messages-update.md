# Endpoints_Communication Broadcast Messages Update

**Method:** PUT
**URL:** `/api/v2//communication/broadcast_messages/`

## Summary
Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//communication/broadcast_messages/:id
Path Parametersid integerrequiredA unique integer value identifying this broadcast message.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredmessagestringrequiredPossible values: non-emptyuse_casestringrequired
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;requiredBodyrequiredmessagestringrequiredPossible values: non-emptyuse_casestringrequired
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;requiredBodyrequiredmessagestringrequiredPossible values: non-emptyuse_casestringrequired
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;required
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;requiredrecipient_countsstringrequired{  "id": 0,  "message": "string",  "use_case": "marketing",  "sent_by": 0,  "is_sent": true,  "sent_at": "2024-07-29T15:51:28.071Z",  "scheduled_at": "2024-07-29T15:51:28.071Z",  "recipient_counts": "string"}SchemaExample (auto)Schemaidintegerrequiredmessagestringrequireduse_casestringrequired
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;requiredrecipient_countsstringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;message&gt;string&lt;/message&gt;  &lt;use_case&gt;marketing&lt;/use_case&gt;  &lt;sent_by&gt;0&lt;/sent_by&gt;  &lt;is_sent&gt;true&lt;/is_sent&gt;  &lt;sent_at&gt;2024-07-29T15:51:28.071Z&lt;/sent_at&gt;  &lt;scheduled_at&gt;2024-07-29T15:51:28.071Z&lt;/scheduled_at&gt;  &lt;recipient_counts&gt;string&lt;/recipient_counts&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "message": "string",  "use_case": "marketing",  "sent_by": 0,  "is_sent": True,  "sent_at": "2024-07-29T15:51:28.071Z",  "scheduled_at": "2024-07-29T15:51:28.071Z"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/communication/broadcast_messages/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"message": "string",
"use_case": "marketing",
## Example Request / Response JSON
```json
{  "id": 0,  "message": "string",  "use_case": "marketing",  "sent_by": 0,  "is_sent": true,  "sent_at": "2024-07-29T15:51:28.071Z",  "scheduled_at": "2024-07-29T15:51:28.071Z",  "recipient_counts": "string"}
```

```json
{  "message": "string",  "use_case": "marketing",  "sent_by": 0,  "is_sent": True,  "sent_at": "2024-07-29T15:51:28.071Z",  "scheduled_at": "2024-07-29T15:51:28.071Z"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"message": "string",
"use_case": "marketing",
"sent_by": 0,
"is_sent": true,
"sent_at": "2024-07-29T15:51:28.071Z",
"scheduled_at": "2024-07-29T15:51:28.071Z"
}
```


