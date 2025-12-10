# Endpoints_Customers Sms Account Retrieve

**Method:** GET
**URL:** `/api/v2//customers/`

## Summary
Sms Account | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customers/:id/sms_account
Path Parametersid integerrequiredA unique integer value identifying this provider customer profile.Query Parameterscountry stringrequiredPossible values: non-emptyenabled booleanrequiredexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]phone_number stringrequiredPossible values: non-emptyHeader ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaverifiedbooleanrequiredcountrystringrequiredfull_numberstringrequiredphone_numberstringrequiredenabledbooleanrequired{  "verified": true,  "country": "string",  "full_number": "string",  "phone_number": "string",  "enabled": true}SchemaExample (auto)Schemaverifiedbooleanrequiredcountrystringrequiredfull_numberstringrequiredphone_numberstringrequiredenabledbooleanrequired&lt;root&gt;  &lt;verified&gt;true&lt;/verified&gt;  &lt;country&gt;string&lt;/country&gt;  &lt;full_number&gt;string&lt;/full_number&gt;  &lt;phone_number&gt;string&lt;/phone_number&gt;  &lt;enabled&gt;true&lt;/enabled&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customers/:id/sms_account", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredcountry — queryrequiredenabled — queryrequired---truefalsephone_number — queryrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousResend Email ConfirmationNextSms AccountCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "verified": true,  "country": "string",  "full_number": "string",  "phone_number": "string",  "enabled": true}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


