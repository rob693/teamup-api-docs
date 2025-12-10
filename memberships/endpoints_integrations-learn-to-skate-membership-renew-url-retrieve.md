# Endpoints_Integrations Learn To Skate Membership Renew Url Retrieve

**Method:** GET
**URL:** `/api/v2//integrations/learn_to_skate/membership_renew_url/`

## Summary
Get membership renewal URL | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//integrations/learn_to_skate/membership_renew_url/:membership_number
The following condition must be met: learn_to_skate_enabled
Path Parametersmembership_number stringrequiredPossible values: Value must match regular expression ^[\w-]+$Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200No response bodyAuthorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/integrations/learn_to_skate/membership_renew_url/:membership_number", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersmembership_number — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousGet current membership numberNextResend consumer membership account linkCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


