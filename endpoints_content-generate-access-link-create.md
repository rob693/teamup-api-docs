# Endpoints_Content Generate Access Link Create

**Method:** POST
**URL:** `/api/v2//content/`

## Summary
Generate Access Link | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//content/:id/generate_access_link
Path Parametersid integerrequiredA unique integer value identifying this content.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaurlstring&lt;uri&gt;requiredis_externalbooleanrequiredoembedrequired{  "url": "string",  "is_external": true,  "oembed": {}}SchemaExample (auto)Schemaurlstring&lt;uri&gt;requiredis_externalbooleanrequiredoembedrequired&lt;root&gt;  &lt;url&gt;string&lt;/url&gt;  &lt;is_external&gt;true&lt;/is_external&gt;  &lt;oembed/&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customer": 0})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/content/:id/generate_access_link", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customer": 0
## Example Request / Response JSON
```json
{  "url": "string",  "is_external": true,  "oembed": {}
```

```json
{  "customer": 0}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"customer": 0
}
```


