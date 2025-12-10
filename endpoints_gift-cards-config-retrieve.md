# Endpoints_Gift Cards Config Retrieve

**Method:** GET
**URL:** `/api/v2//gift_cards/config`

## Summary
Gift Card Config | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//gift_cards/config
Must have one of the following permissions: super_admin, store, pos.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaidintegerrequiredis_enabled_provider_sitebooleanrequiredis_enabled_customer_sitebooleanrequiredimage_choices object[]requiredArray [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [image]urlstring&lt;uri&gt;requiredprofileintegernullableoriginal_widthintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647original_heightintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647userintegernullablecreated_atstring&lt;date-time&gt;required]amount_choicesrequireddo_gift_cards_expirebooleanrequiredredemption_expiration_daysintegerrequiredredemption_email_template objectrequiredsubjectstringrequiredbodystringrequired{  "id": 0,  "is_enabled_provider_site": true,  "is_enabled_customer_site": true,  "image_choices": [    {      "id": 0,      "url": "string",      "profile": 0,      "original_width": 0,      "original_height": 0,      "user": 0,      "created_at": "2024-07-29T15:51:28.071Z"    }  ],  "amount_choices": {},  "do_gift_cards_expire": true,  "redemption_expiration_days": 0,  "redemption_email_template": {    "subject": "string",    "body": "string"  }}SchemaExample (auto)Schemaidintegerrequiredis_enabled_provider_sitebooleanrequiredis_enabled_customer_sitebooleanrequiredimage_choices object[]requiredArray [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [image]urlstring&lt;uri&gt;requiredprofileintegernullableoriginal_widthintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647original_heightintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647userintegernullablecreated_atstring&lt;date-time&gt;required]amount_choicesrequireddo_gift_cards_expirebooleanrequiredredemption_expiration_daysintegerrequiredredemption_email_template objectrequiredsubjectstringrequiredbodystringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;is_enabled_provider_site&gt;true&lt;/is_enabled_provider_site&gt;  &lt;is_enabled_customer_site&gt;true&lt;/is_enabled_customer_site&gt;  &lt;image_choices&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;url&gt;string&lt;/url&gt;    &lt;profile&gt;0&lt;/profile&gt;    &lt;original_width&gt;0&lt;/original_width&gt;    &lt;original_height&gt;0&lt;/original_height&gt;    &lt;user&gt;0&lt;/user&gt;    &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;  &lt;/image_choices&gt;  &lt;amount_choices/&gt;  &lt;do_gift_cards_expire&gt;true&lt;/do_gift_cards_expire&gt;  &lt;redemption_expiration_days&gt;0&lt;/redemption_expiration_days&gt;  &lt;redemption_email_template&gt;    &lt;subject&gt;string&lt;/subject&gt;    &lt;body&gt;string&lt;/body&gt;  &lt;/redemption_email_template&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/gift_cards/config", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousRedeem Gift CardNextUpdate ConfigCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "is_enabled_provider_site": true,  "is_enabled_customer_site": true,  "image_choices": [    {      "id": 0,      "url": "string",      "profile": 0,      "original_width": 0,      "original_height": 0,      "user": 0,      "created_at": "2024-07-29T15:51:28.071Z"    }
```

```json
{}
```

```json
{    "subject": "string",    "body": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


