# Endpoints_Customer Membership Holds Payment Resolution Retrieve

**Method:** GET
**URL:** `/api/v2//customer_membership_holds/`

## Summary
Get payment resolution for a membership hold | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//customer_membership_holds/:id/payment_resolution
Path Parametersid integerrequiredA unique integer value identifying this consumer membership hold.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaprorate_strategystringreactivation_billing_periodobjectnullableresolutionobjectnullablestart_billing_periodobjectnullable{  "prorate_strategy": "string",  "reactivation_billing_period": {},  "resolution": {},  "start_billing_period": {}}SchemaExample (auto)Schemaprorate_strategystringreactivation_billing_periodobjectnullableresolutionobjectnullablestart_billing_periodobjectnullable&lt;root&gt;  &lt;prorate_strategy&gt;string&lt;/prorate_strategy&gt;  &lt;reactivation_billing_period/&gt;  &lt;resolution/&gt;  &lt;start_billing_period/&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/customer_membership_holds/:id/payment_resolution", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousRetrieve a specific membership holdNextCustomer MembershipsCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "prorate_strategy": "string",  "reactivation_billing_period": {}
```

```json
{}
```

```json
{}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


