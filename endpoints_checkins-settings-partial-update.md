# Endpoints_Checkins Settings Partial Update

**Method:** PATCH
**URL:** `/api/v2//checkins/settings`

## Summary
checkins_settings_partial_update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//checkins/settings
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyenabledbooleangranularitystringPossible values: [business, venue]BodyenabledbooleangranularitystringPossible values: [business, venue]BodyenabledbooleangranularitystringPossible values: [business, venue]
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaenabledbooleangranularitystringrequiredPossible values: [business, venue]{  "enabled": true,  "granularity": "business"}SchemaExample (auto)SchemaenabledbooleangranularitystringrequiredPossible values: [business, venue]&lt;root&gt;  &lt;enabled&gt;true&lt;/enabled&gt;  &lt;granularity&gt;business&lt;/granularity&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "enabled": True,  "granularity": "business"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/checkins/settings", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"enabled": true,
"granularity": "business"
## Example Request / Response JSON
```json
{  "enabled": true,  "granularity": "business"}
```

```json
{  "enabled": True,  "granularity": "business"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"enabled": true,
"granularity": "business"
}
```


