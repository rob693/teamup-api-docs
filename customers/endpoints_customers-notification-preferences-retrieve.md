# Endpoints_Customers Notification Preferences Retrieve

**Method:** GET
**URL:** `/api/v2//customers/`

## Summary
Notification Preferences | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customers/:id/notification_preferences
Path Parametersid integerrequiredA unique integer value identifying this provider customer profile.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [customer_notification_preference]typestringrequireddescriptionstringrequiredsms_enabledbooleanrequiredemail_enabledbooleanrequiredcapabilities objectrequiredFor a notification to be SMS-compatible the following must be true:
property name*anyFor a notification to be SMS-compatible the following must be true:
toggleability objectrequiredproperty name*any{  "id": 0,  "type": "string",  "description": "string",  "sms_enabled": true,  "email_enabled": true,  "capabilities": {},  "toggleability": {}}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [customer_notification_preference]typestringrequireddescriptionstringrequiredsms_enabledbooleanrequiredemail_enabledbooleanrequiredcapabilities objectrequiredFor a notification to be SMS-compatible the following must be true:
property name*anyFor a notification to be SMS-compatible the following must be true:
toggleability objectrequiredproperty name*any&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;type&gt;string&lt;/type&gt;  &lt;description&gt;string&lt;/description&gt;  &lt;sms_enabled&gt;true&lt;/sms_enabled&gt;  &lt;email_enabled&gt;true&lt;/email_enabled&gt;  &lt;capabilities/&gt;  &lt;toggleability/&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customers/:id/notification_preferences", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousIcalendar LinksNextUpdate Notification PreferenceCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "type": "string",  "description": "string",  "sms_enabled": true,  "email_enabled": true,  "capabilities": {}
```

```json
{}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


