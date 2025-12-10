# Endpoints_Integrations Learn To Skate Abandon Membership Create

**Method:** POST
**URL:** `/api/v2//integrations/learn_to_skate/abandon_membership`

## Summary
Abandon consumer membership | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//integrations/learn_to_skate/abandon_membership
The following condition must be met: learn_to_skate_enabled
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodymembership_numberstringPossible values: non-empty and &lt;= 10 charactersBodymembership_numberstringPossible values: non-empty and &lt;= 10 charactersBodymembership_numberstringPossible values: non-empty and &lt;= 10 characters
Responses​200No response bodyAuthorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "membership_number": "string"})headers = {  'Content-Type': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/integrations/learn_to_skate/abandon_membership", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"membership_number": "string"
## Example Request / Response JSON
```json
{  "membership_number": "string"}
```

```json
{  'Content-Type': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"membership_number": "string"
}
```


