# Endpoints_Customer Forms Destroy

**Method:** DELETE
**URL:** `/api/v2//customer_forms/`

## Summary
Delete Customer Form | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

DELETE https://goteamup.com/api/v2//customer_forms/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this form.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​204No response bodyAuthorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("DELETE", "/api/v2/customer_forms/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousPartially Update Customer FormNextChange Customer Form OrderCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


