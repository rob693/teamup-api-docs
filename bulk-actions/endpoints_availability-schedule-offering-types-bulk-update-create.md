# Endpoints_Availability Schedule Offering Types Bulk Update Create

**Method:** POST
**URL:** `/api/v2//availability_schedule_offering_types/bulk_update`

## Summary
Bulk Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//availability_schedule_offering_types/bulk_update
Must have one of the following permissions: manage_events.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​204No response bodyAuthorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "items": [    {      "offering_type": 0,      "availability_schedule": 0,      "venue_rooms": [        0      ]    }  ]})headers = {  'Content-Type': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/availability_schedule_offering_types/bulk_update", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"items": [
"offering_type": 0,
"availability_schedule": 0,
"venue_rooms": [
## Example Request / Response JSON
```json
{  "items": [    {      "offering_type": 0,      "availability_schedule": 0,      "venue_rooms": [        0      ]    }
```

```json
{  'Content-Type': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"items": [
{
"offering_type": 0,
"availability_schedule": 0,
"venue_rooms": [
0
]
}
```


