# Endpoints_Gift Cards Config Metadata Retrieve

**Method:** GET
**URL:** `/api/v2//gift_cards/config/metadata`

## Summary
Get Gift Card Metadata | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//gift_cards/config/metadata
Must have one of the following permissions: super_admin, store, pos.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schematemplate_variables object[]Array [namestringdescriptionstringsample_valuestring]multiple_messages_allowedboolean{  "template_variables": [    {      "name": "string",      "description": "string",      "sample_value": "string"    }  ],  "multiple_messages_allowed": true}SchemaExample (auto)Schematemplate_variables object[]Array [namestringdescriptionstringsample_valuestring]multiple_messages_allowedboolean&lt;root&gt;  &lt;template_variables&gt;    &lt;name&gt;string&lt;/name&gt;    &lt;description&gt;string&lt;/description&gt;    &lt;sample_value&gt;string&lt;/sample_value&gt;  &lt;/template_variables&gt;  &lt;multiple_messages_allowed&gt;true&lt;/multiple_messages_allowed&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/gift_cards/config/metadata", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousUpdate ConfigNextImagesCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "template_variables": [    {      "name": "string",      "description": "string",      "sample_value": "string"    }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


