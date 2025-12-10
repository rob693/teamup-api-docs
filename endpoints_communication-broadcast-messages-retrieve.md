# Endpoints_Communication Broadcast Messages Retrieve

**Method:** GET
**URL:** `/api/v2//communication/broadcast_messages/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//communication/broadcast_messages/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this broadcast message.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;requiredrecipient_countsstringrequired{  "id": 0,  "message": "string",  "use_case": "marketing",  "sent_by": 0,  "is_sent": true,  "sent_at": "2024-07-29T15:51:28.071Z",  "scheduled_at": "2024-07-29T15:51:28.071Z",  "recipient_counts": "string"}SchemaExample (auto)Schemaidintegerrequiredmessagestringrequireduse_casestringrequired
Possible values: [marketing, general]sent_byintegerrequiredis_sentbooleanrequiredsent_atstring&lt;date-time&gt;requiredscheduled_atstring&lt;date-time&gt;requiredrecipient_countsstringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;message&gt;string&lt;/message&gt;  &lt;use_case&gt;marketing&lt;/use_case&gt;  &lt;sent_by&gt;0&lt;/sent_by&gt;  &lt;is_sent&gt;true&lt;/is_sent&gt;  &lt;sent_at&gt;2024-07-29T15:51:28.071Z&lt;/sent_at&gt;  &lt;scheduled_at&gt;2024-07-29T15:51:28.071Z&lt;/scheduled_at&gt;  &lt;recipient_counts&gt;string&lt;/recipient_counts&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/communication/broadcast_messages/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCreateNextUpdateCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "message": "string",  "use_case": "marketing",  "sent_by": 0,  "is_sent": true,  "sent_at": "2024-07-29T15:51:28.071Z",  "scheduled_at": "2024-07-29T15:51:28.071Z",  "recipient_counts": "string"}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


