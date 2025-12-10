# Endpoints_Providers Trial Status Retrieve

**Method:** GET
**URL:** `/api/v2//providers/`

## Summary
Trial Status | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//providers/:id/trial_status
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this provider profile.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemastatusstringrequiredPossible values: [pending, ongoing, unknown]has_payment_methodbooleanrequiredbilling_datestring&lt;date&gt;requiredis_blockedbooleanrequiredtrial_customers_countintegerrequireddays_totalintegerrequireddays_remainingintegerrequiredshow_chatbooleanrequiredonly_customer objectnullableidintegerrequirednamestringrequired{  "status": "pending",  "has_payment_method": true,  "billing_date": "2024-07-29",  "is_blocked": true,  "trial_customers_count": 0,  "days_total": 0,  "days_remaining": 0,  "show_chat": true,  "only_customer": {    "id": 0,    "name": "string"  }}SchemaExample (auto)SchemastatusstringrequiredPossible values: [pending, ongoing, unknown]has_payment_methodbooleanrequiredbilling_datestring&lt;date&gt;requiredis_blockedbooleanrequiredtrial_customers_countintegerrequireddays_totalintegerrequireddays_remainingintegerrequiredshow_chatbooleanrequiredonly_customer objectnullableidintegerrequirednamestringrequired&lt;root&gt;  &lt;status&gt;pending&lt;/status&gt;  &lt;has_payment_method&gt;true&lt;/has_payment_method&gt;  &lt;billing_date&gt;2024-07-29&lt;/billing_date&gt;  &lt;is_blocked&gt;true&lt;/is_blocked&gt;  &lt;trial_customers_count&gt;0&lt;/trial_customers_count&gt;  &lt;days_total&gt;0&lt;/days_total&gt;  &lt;days_remaining&gt;0&lt;/days_remaining&gt;  &lt;show_chat&gt;true&lt;/show_chat&gt;  &lt;only_customer&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;  &lt;/only_customer&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/providers/:id/trial_status", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousUpdate ThemeNextPurchase FeesCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "status": "pending",  "has_payment_method": true,  "billing_date": "2024-07-29",  "is_blocked": true,  "trial_customers_count": 0,  "days_total": 0,  "days_remaining": 0,  "show_chat": true,  "only_customer": {    "id": 0,    "name": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


