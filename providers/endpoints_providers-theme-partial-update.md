# Endpoints_Providers Theme Partial Update

**Method:** PATCH
**URL:** `/api/v2//providers/`

## Summary
Update Theme | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//providers/:id/theme
Must have one of the following permissions: super_admin, developer.
Path Parametersid integerrequiredA unique integer value identifying this provider profile.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyhomescreen_logo objectnullableidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64Bodyhomescreen_logo objectnullableidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64Bodyhomescreen_logo objectnullableidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [provider_theme]homescreen_logo objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64{  "id": 0,  "homescreen_logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [provider_theme]homescreen_logo objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;homescreen_logo&gt;    &lt;id&gt;13314&lt;/id&gt;    &lt;url&gt;string&lt;/url&gt;    &lt;original_width&gt;64&lt;/original_width&gt;    &lt;original_height&gt;64&lt;/original_height&gt;  &lt;/homescreen_logo&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "homescreen_logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/providers/:id/theme", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"homescreen_logo": {
"id": 13314,
"url": "string",
"original_width": 64,
"original_height": 64
## Example Request / Response JSON
```json
{  "id": 0,  "homescreen_logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }
```

```json
{  "homescreen_logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"homescreen_logo": {
"id": 13314,
"url": "string",
"original_width": 64,
"original_height": 64
}
```


