# Endpoints_Discount Code Applicabilities Update

**Method:** PUT
**URL:** `/api/v2//discount_code_applicabilities/`

## Summary
Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//discount_code_applicabilities/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this discount code applicable object.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [store_product, offering_type, membership, event, course]Bodyrequireddiscount_codeintegerrequiredallow_usebooleanitem objectrequiredidintegerrequiredtypestringrequired
Possible values: [store_product, offering_type, membership, event, course]Bodyrequireddiscount_codeintegerrequiredallow_usebooleanitem objectrequiredidintegerrequiredtypestringrequired
Possible values: [store_product, offering_type, membership, event, course]
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [discount_code_applicability]allow_usebooleanitemstringrequireddiscount_codeintegerrequired{  "id": 0,  "allow_use": true,  "item": "string",  "discount_code": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [discount_code_applicability]allow_usebooleanitemstringrequireddiscount_codeintegerrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;allow_use&gt;true&lt;/allow_use&gt;  &lt;item&gt;string&lt;/item&gt;  &lt;discount_code&gt;0&lt;/discount_code&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "discount_code": 0,  "allow_use": True,  "item": {    "id": 0,    "type": "store_product"  }})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/discount_code_applicabilities/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"discount_code": 0,
"allow_use": true,
"item": {
## Example Request / Response JSON
```json
{  "id": 0,  "allow_use": true,  "item": "string",  "discount_code": 0}
```

```json
{  "discount_code": 0,  "allow_use": True,  "item": {    "id": 0,    "type": "store_product"  }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"discount_code": 0,
"allow_use": true,
"item": {
"id": 0,
"type": "store_product"
}
```


