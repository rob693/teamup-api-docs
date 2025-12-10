# Endpoints_Integrations Learn To Skate Verify Membership Create

**Method:** POST
**URL:** `/api/v2//integrations/learn_to_skate/verify_membership`

## Summary
Verify consumer membership | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//integrations/learn_to_skate/verify_membership
The following condition must be met: learn_to_skate_enabled
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredmembership_numberstringrequiredPossible values: non-empty and &lt;= 10 charactersBodyrequiredmembership_numberstringrequiredPossible values: non-empty and &lt;= 10 charactersBodyrequiredmembership_numberstringrequiredPossible values: non-empty and &lt;= 10 characters
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemamembership_numberstringrequiredPossible values: non-empty and &lt;= 10 charactersexpirationstring&lt;date-time&gt;requiredis_expiredbooleanrequiredunverified_error_detailstringrequiredstatusintegerrequired
Possible values: [0, 1, 2, 3]{  "membership_number": "string",  "expiration": "2024-07-29T15:51:28.071Z",  "is_expired": true,  "unverified_error_detail": "string",  "status": 0}SchemaExample (auto)Schemamembership_numberstringrequiredPossible values: non-empty and &lt;= 10 charactersexpirationstring&lt;date-time&gt;requiredis_expiredbooleanrequiredunverified_error_detailstringrequiredstatusintegerrequired
Possible values: [0, 1, 2, 3]&lt;root&gt;  &lt;membership_number&gt;string&lt;/membership_number&gt;  &lt;expiration&gt;2024-07-29T15:51:28.071Z&lt;/expiration&gt;  &lt;is_expired&gt;true&lt;/is_expired&gt;  &lt;unverified_error_detail&gt;string&lt;/unverified_error_detail&gt;  &lt;status&gt;0&lt;/status&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "membership_number": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/integrations/learn_to_skate/verify_membership", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"membership_number": "string"
## Example Request / Response JSON
```json
{  "membership_number": "string",  "expiration": "2024-07-29T15:51:28.071Z",  "is_expired": true,  "unverified_error_detail": "string",  "status": 0}
```

```json
{  "membership_number": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"membership_number": "string"
}
```


