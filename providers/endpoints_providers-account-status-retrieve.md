# Endpoints_Providers Account Status Retrieve

**Method:** GET
**URL:** `/api/v2//providers/`

## Summary
Account Status | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//providers/:id/account_status
Path Parametersid integerrequiredA unique integer value identifying this provider profile.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemalocked_outbooleanrequiredlock_out_override_appliedbooleanrequiredteamup_billing objectnullablein_retrybooleanrequiredretry_countintegerrequiredpayment_errors object[]requiredArray [attempt_datestring&lt;date&gt;requireddetailsstringrequired]subscription objectnullablerequiredidintegerrequiredhas_payment_methodbooleanrequiredis_compedbooleanrequiredfranchise_fee_issues object[]nullablerequiredArray [statusstringrequiredmanager objectrequirednamestringrequired]go_cardless objectnullableverifiedbooleanrequiredverify_urlstringrequiredstripe objectnullablecharges_enabledbooleanrequiredpayouts_enabledbooleanrequiredverify_current_deadlinestring&lt;date-time&gt;nullablerequiredstripe_dashboard_urlstringrequired{  "locked_out": true,  "lock_out_override_applied": true,  "teamup_billing": {    "in_retry": true,    "retry_count": 0,    "payment_errors": [      {        "attempt_date": "2024-07-29",        "details": "string"      }    ],    "subscription": {      "id": 0    },    "has_payment_method": true,    "is_comped": true  },  "franchise_fee_issues": [    {      "status": "string",      "manager": {        "name": "string"      }    }  ],  "go_cardless": {    "verified": true,    "verify_url": "string"  },  "stripe": {    "charges_enabled": true,    "payouts_enabled": true,    "verify_current_deadline": "2024-07-29T15:51:28.071Z",    "stripe_dashboard_url": "string"  }}SchemaExample (auto)Schemalocked_outbooleanrequiredlock_out_override_appliedbooleanrequiredteamup_billing objectnullablein_retrybooleanrequiredretry_countintegerrequiredpayment_errors object[]requiredArray [attempt_datestring&lt;date&gt;requireddetailsstringrequired]subscription objectnullablerequiredidintegerrequiredhas_payment_methodbooleanrequiredis_compedbooleanrequiredfranchise_fee_issues object[]nullablerequiredArray [statusstringrequiredmanager objectrequirednamestringrequired]go_cardless objectnullableverifiedbooleanrequiredverify_urlstringrequiredstripe objectnullablecharges_enabledbooleanrequiredpayouts_enabledbooleanrequiredverify_current_deadlinestring&lt;date-time&gt;nullablerequiredstripe_dashboard_urlstringrequired&lt;root&gt;  &lt;locked_out&gt;true&lt;/locked_out&gt;  &lt;lock_out_override_applied&gt;true&lt;/lock_out_override_applied&gt;  &lt;teamup_billing&gt;    &lt;in_retry&gt;true&lt;/in_retry&gt;    &lt;retry_count&gt;0&lt;/retry_count&gt;    &lt;payment_errors&gt;      &lt;attempt_date&gt;2024-07-29&lt;/attempt_date&gt;      &lt;details&gt;string&lt;/details&gt;    &lt;/payment_errors&gt;    &lt;subscription&gt;      &lt;id&gt;0&lt;/id&gt;    &lt;/subscription&gt;    &lt;has_payment_method&gt;true&lt;/has_payment_method&gt;    &lt;is_comped&gt;true&lt;/is_comped&gt;  &lt;/teamup_billing&gt;  &lt;franchise_fee_issues&gt;    &lt;status&gt;string&lt;/status&gt;    &lt;manager&gt;      &lt;name&gt;string&lt;/name&gt;    &lt;/manager&gt;  &lt;/franchise_fee_issues&gt;  &lt;go_cardless&gt;    &lt;verified&gt;true&lt;/verified&gt;    &lt;verify_url&gt;string&lt;/verify_url&gt;  &lt;/go_cardless&gt;  &lt;stripe&gt;    &lt;charges_enabled&gt;true&lt;/charges_enabled&gt;    &lt;payouts_enabled&gt;true&lt;/payouts_enabled&gt;    &lt;verify_current_deadline&gt;2024-07-29T15:51:28.071Z&lt;/verify_current_deadline&gt;    &lt;stripe_dashboard_url&gt;string&lt;/stripe_dashboard_url&gt;  &lt;/stripe&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/providers/:id/account_status", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousRetrieveNextCustomer Referral SettingsCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "locked_out": true,  "lock_out_override_applied": true,  "teamup_billing": {    "in_retry": true,    "retry_count": 0,    "payment_errors": [      {        "attempt_date": "2024-07-29",        "details": "string"      }
```

```json
{      "id": 0    }
```

```json
{      "status": "string",      "manager": {        "name": "string"      }
```

```json
{    "verified": true,    "verify_url": "string"  }
```

```json
{    "charges_enabled": true,    "payouts_enabled": true,    "verify_current_deadline": "2024-07-29T15:51:28.071Z",    "stripe_dashboard_url": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


