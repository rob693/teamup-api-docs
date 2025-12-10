# Endpoints_Memberships Allotment Update

**Method:** PUT
**URL:** `/api/v2//memberships/`

## Summary
Update Allotment | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//memberships/:id/allotment
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this membership.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredignore_no_showsbooleanDefault value: falsetypesstring[]requiredPossible values: &gt;= 1period_limits object[]requiredArray [max_usesintegerrequiredperiodstringrequiredtypestringrequiredThe type of offering the periodic limit applies to. One of: event, class, course.offering_type_limits object[]requiredArray [offering_typeintegerrequiredmax_usesintegerrequiredis_extrabooleanrequired]]Bodyrequiredignore_no_showsbooleanDefault value: falsetypesstring[]requiredPossible values: &gt;= 1period_limits object[]requiredArray [max_usesintegerrequiredperiodstringrequiredtypestringrequiredThe type of offering the periodic limit applies to. One of: event, class, course.offering_type_limits object[]requiredArray [offering_typeintegerrequiredmax_usesintegerrequiredis_extrabooleanrequired]]Bodyrequiredignore_no_showsbooleanDefault value: falsetypesstring[]requiredPossible values: &gt;= 1period_limits object[]requiredArray [max_usesintegerrequiredperiodstringrequiredtypestringrequiredThe type of offering the periodic limit applies to. One of: event, class, course.offering_type_limits object[]requiredArray [offering_typeintegerrequiredmax_usesintegerrequiredis_extrabooleanrequired]]
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemastatusstringrequiredConstant value: OKPossible values: [OK]detailstringnullablerequired{  "status": "OK",  "detail": "string"}SchemaExample (auto)SchemastatusstringrequiredConstant value: OKPossible values: [OK]detailstringnullablerequired&lt;root&gt;  &lt;status&gt;OK&lt;/status&gt;  &lt;detail&gt;string&lt;/detail&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "ignore_no_shows": False,  "types": [    "string"  ],  "period_limits": [    {      "max_uses": 0,      "period": "string",      "type": "string",      "offering_type_limits": [        {          "offering_type": 0,          "max_uses": 0,          "is_extra": True        }      ]    }  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/memberships/:id/allotment", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"ignore_no_shows": false,
"types": [
"period_limits": [
"max_uses": 0,
"period": "string",
## Example Request / Response JSON
```json
{  "status": "OK",  "detail": "string"}
```

```json
{  "ignore_no_shows": False,  "types": [    "string"  ],  "period_limits": [    {      "max_uses": 0,      "period": "string",      "type": "string",      "offering_type_limits": [        {          "offering_type": 0,          "max_uses": 0,          "is_extra": True        }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"ignore_no_shows": false,
"types": [
"string"
],
"period_limits": [
{
"max_uses": 0,
"period": "string",
"type": "string",
"offering_type_limits": [
{
"offering_type": 0,
"max_uses": 0,
"is_extra": true
}
```


