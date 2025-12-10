# Endpoints_Gift Cards Config Partial Update

**Method:** PATCH
**URL:** `/api/v2//gift_cards/config`

## Summary
Update Config | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//gift_cards/config
Must have one of the following permissions: super_admin, store, pos.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyis_enabled_provider_sitebooleanis_enabled_customer_sitebooleanimage_choicesinteger[]amount_choicesdo_gift_cards_expirebooleanredemption_expiration_daysintegerredemption_email_template objectsubjectstringrequiredPossible values: non-emptybodystringrequiredPossible values: non-emptyBodyis_enabled_provider_sitebooleanis_enabled_customer_sitebooleanimage_choicesinteger[]amount_choicesdo_gift_cards_expirebooleanredemption_expiration_daysintegerredemption_email_template objectsubjectstringrequiredPossible values: non-emptybodystringrequiredPossible values: non-emptyBodyis_enabled_provider_sitebooleanis_enabled_customer_sitebooleanimage_choicesinteger[]amount_choicesdo_gift_cards_expirebooleanredemption_expiration_daysintegerredemption_email_template objectsubjectstringrequiredPossible values: non-emptybodystringrequiredPossible values: non-empty
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaidintegerrequiredis_enabled_provider_sitebooleanrequiredis_enabled_customer_sitebooleanrequiredimage_choices object[]requiredArray [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [image]urlstring&lt;uri&gt;requiredprofileintegernullableoriginal_widthintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647original_heightintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647userintegernullablecreated_atstring&lt;date-time&gt;required]amount_choicesrequireddo_gift_cards_expirebooleanrequiredredemption_expiration_daysintegerrequiredredemption_email_template objectrequiredsubjectstringrequiredbodystringrequired{  "id": 0,  "is_enabled_provider_site": true,  "is_enabled_customer_site": true,  "image_choices": [    {      "id": 0,      "url": "string",      "profile": 0,      "original_width": 0,      "original_height": 0,      "user": 0,      "created_at": "2024-07-29T15:51:28.071Z"    }  ],  "amount_choices": {},  "do_gift_cards_expire": true,  "redemption_expiration_days": 0,  "redemption_email_template": {    "subject": "string",    "body": "string"  }}SchemaExample (auto)Schemaidintegerrequiredis_enabled_provider_sitebooleanrequiredis_enabled_customer_sitebooleanrequiredimage_choices object[]requiredArray [idintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [image]urlstring&lt;uri&gt;requiredprofileintegernullableoriginal_widthintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647original_heightintegernullablePossible values: &gt;= -2147483648 and &lt;= 2147483647userintegernullablecreated_atstring&lt;date-time&gt;required]amount_choicesrequireddo_gift_cards_expirebooleanrequiredredemption_expiration_daysintegerrequiredredemption_email_template objectrequiredsubjectstringrequiredbodystringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;is_enabled_provider_site&gt;true&lt;/is_enabled_provider_site&gt;  &lt;is_enabled_customer_site&gt;true&lt;/is_enabled_customer_site&gt;  &lt;image_choices&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;url&gt;string&lt;/url&gt;    &lt;profile&gt;0&lt;/profile&gt;    &lt;original_width&gt;0&lt;/original_width&gt;    &lt;original_height&gt;0&lt;/original_height&gt;    &lt;user&gt;0&lt;/user&gt;    &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;  &lt;/image_choices&gt;  &lt;amount_choices/&gt;  &lt;do_gift_cards_expire&gt;true&lt;/do_gift_cards_expire&gt;  &lt;redemption_expiration_days&gt;0&lt;/redemption_expiration_days&gt;  &lt;redemption_email_template&gt;    &lt;subject&gt;string&lt;/subject&gt;    &lt;body&gt;string&lt;/body&gt;  &lt;/redemption_email_template&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "is_enabled_provider_site": True,  "is_enabled_customer_site": True,  "image_choices": [    0  ],  "amount_choices": {},  "do_gift_cards_expire": True,  "redemption_expiration_days": 0,  "redemption_email_template": {    "subject": "string",    "body": "string"  }})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/gift_cards/config", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"is_enabled_provider_site": true,
"is_enabled_customer_site": true,
"image_choices": [
"amount_choices": {},
"do_gift_cards_expire": true,
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
{  "is_enabled_provider_site": True,  "is_enabled_customer_site": True,  "image_choices": [    0  ],  "amount_choices": {}
```

```json
{    "subject": "string",    "body": "string"  }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"is_enabled_provider_site": true,
"is_enabled_customer_site": true,
"image_choices": [
0
],
"amount_choices": {}
```

```json
{
"subject": "string",
"body": "string"
}
```


