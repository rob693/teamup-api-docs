# Endpoints_Auth Two Factor Requirements Retrieve

**Method:** GET
**URL:** `/api/v2//auth/two_factor/requirements`

## Summary
Check 2FA Requirements | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//auth/two_factor/requirements
Query Parametersformat stringPossible values: [json, xml]provider integerrequired
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemais_sms_enabledbooleanrequiredis_2fa_required_for_registrationbooleanrequiredis_2fa_required_for_loginbooleanrequired{  "is_sms_enabled": true,  "is_2fa_required_for_registration": true,  "is_2fa_required_for_login": true}SchemaExample (auto)Schemais_sms_enabledbooleanrequiredis_2fa_required_for_registrationbooleanrequiredis_2fa_required_for_loginbooleanrequired&lt;root&gt;  &lt;is_sms_enabled&gt;true&lt;/is_sms_enabled&gt;  &lt;is_2fa_required_for_registration&gt;true&lt;/is_2fa_required_for_registration&gt;  &lt;is_2fa_required_for_login&gt;true&lt;/is_2fa_required_for_login&gt;&lt;/root&gt;pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json'}conn.request("GET", "/api/v2/auth/two_factor/requirements", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2Parametersprovider — queryrequiredShow optional parametersformat — query---jsonxmlSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousTwo Factor AuthNextStart 2FA VerificationCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "is_sms_enabled": true,  "is_2fa_required_for_registration": true,  "is_2fa_required_for_login": true}
```

```json
{  'Accept': 'application/json'}
```


