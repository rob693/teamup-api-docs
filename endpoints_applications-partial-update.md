# Endpoints_Applications Partial Update

**Method:** PATCH
**URL:** `/api/v2//applications/`

## Summary
Partially Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//applications/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this application.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodynamestringPossible values: non-emptydomainstringPossible values: non-emptylogointegernullableThe unique identifier of the image you'd like to associate with this object.Example: 4242typestringPossible values: [customer, provider]scopesstring[]Possible values: [read, read_write]allowed_callback_urlsstring&lt;uri&gt;[]Possible values: non-emptyBodynamestringPossible values: non-emptydomainstringPossible values: non-emptylogointegernullableThe unique identifier of the image you'd like to associate with this object.Example: 4242typestringPossible values: [customer, provider]scopesstring[]Possible values: [read, read_write]allowed_callback_urlsstring&lt;uri&gt;[]Possible values: non-emptyBodynamestringPossible values: non-emptydomainstringPossible values: non-emptylogointegernullableThe unique identifier of the image you'd like to associate with this object.Example: 4242typestringPossible values: [customer, provider]scopesstring[]Possible values: [read, read_write]allowed_callback_urlsstring&lt;uri&gt;[]Possible values: non-empty
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [application]namestringrequireddomainstringnullablePossible values: &lt;= 255 characterslogo objectrequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64typestringrequiredPossible values: [customer, provider]scopesstring[]requiredPossible values: [read, read_write]allowed_callback_urlsstring[]requiredaccess_tokens object[]requiredArray [keystring]client_idstringPossible values: &lt;= 100 charactersclient_secretstringPossible values: &lt;= 255 characters{  "id": 0,  "name": "string",  "domain": "string",  "logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  },  "type": "customer",  "scopes": [    "read"  ],  "allowed_callback_urls": [    "string"  ],  "access_tokens": [    {      "key": "string"    }  ],  "client_id": "string",  "client_secret": "string"}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [application]namestringrequireddomainstringnullablePossible values: &lt;= 255 characterslogo objectrequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64typestringrequiredPossible values: [customer, provider]scopesstring[]requiredPossible values: [read, read_write]allowed_callback_urlsstring[]requiredaccess_tokens object[]requiredArray [keystring]client_idstringPossible values: &lt;= 100 charactersclient_secretstringPossible values: &lt;= 255 characters&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;domain&gt;string&lt;/domain&gt;  &lt;logo&gt;    &lt;id&gt;13314&lt;/id&gt;    &lt;url&gt;string&lt;/url&gt;    &lt;original_width&gt;64&lt;/original_width&gt;    &lt;original_height&gt;64&lt;/original_height&gt;  &lt;/logo&gt;  &lt;type&gt;customer&lt;/type&gt;  &lt;scopes&gt;read&lt;/scopes&gt;  &lt;allowed_callback_urls&gt;string&lt;/allowed_callback_urls&gt;  &lt;access_tokens&gt;    &lt;key&gt;string&lt;/key&gt;  &lt;/access_tokens&gt;  &lt;client_id&gt;string&lt;/client_id&gt;  &lt;client_secret&gt;string&lt;/client_secret&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "name": "string",  "domain": "string",  "logo": 4242,  "type": "customer",  "scopes": [    "read"  ],  "allowed_callback_urls": [    "string"  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/applications/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"name": "string",
"domain": "string",
"logo": 4242,
"type": "customer",
"scopes": [
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "domain": "string",  "logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }
```

```json
{      "key": "string"    }
```

```json
{  "name": "string",  "domain": "string",  "logo": 4242,  "type": "customer",  "scopes": [    "read"  ],  "allowed_callback_urls": [    "string"  ]}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"domain": "string",
"logo": 4242,
"type": "customer",
"scopes": [
"read"
],
"allowed_callback_urls": [
"string"
]
}
```


