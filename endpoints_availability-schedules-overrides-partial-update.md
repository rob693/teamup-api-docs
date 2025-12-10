# Endpoints_Availability Schedules Overrides Partial Update

**Method:** PATCH
**URL:** `/api/v2//availability_schedules/`

## Summary
Update Overrides | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//availability_schedules/:id/overrides
Must have one of the following permissions: manage_events.
The following condition must be met: object_is_own_schedule
Path Parametersid stringrequiredQuery Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​204No response bodyAuthorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "overrides": [    {      "date": "2024-07-29",      "availability": [        {          "start": "string",          "end": "string"        }      ]    }  ]})headers = {  'Content-Type': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/availability_schedules/:id/overrides", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"overrides": [
"date": "2024-07-29",
"availability": [
"start": "string",
"end": "string"
## Example Request / Response JSON
```json
{  "overrides": [    {      "date": "2024-07-29",      "availability": [        {          "start": "string",          "end": "string"        }
```

```json
{  'Content-Type': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"overrides": [
{
"date": "2024-07-29",
"availability": [
{
"start": "string",
"end": "string"
}
```


