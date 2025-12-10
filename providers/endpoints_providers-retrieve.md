# Endpoints_Providers Retrieve

**Method:** GET
**URL:** `/api/v2//providers/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//providers/:id
Path Parametersid integerrequiredA unique integer value identifying this provider profile.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [provider]namestringrequiredPossible values: &lt;= 255 charactersdescriptionstringlogo objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64countrystringrequiredcurrency objectrequirediso_currency_codestringrequiredsymbolstringrequiredpositionstringrequired
Possible values: [before, after]is_marketing_preference_on_customer_formsbooleanrequiredicalendar_links object DeferredThis field is DEFERRED.linkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]requiredcontact_info object DeferredThis field is DEFERRED.emailstringnullablerequiredphone_numberstringnullablerequireddefault_registration_settings object DeferredThis field is DEFERRED.registrations_open_intervalstringrequiredregistrations_close_intervalstringrequiredcancellation_notice_intervalstringrequiredaddress object DeferredThis field is DEFERRED.streetstringrequiredstreet_secondarystringnullablerequiredcitystringrequiredregionstringnullablerequiredpostal_codestringrequiredcountrystringrequiredtimezonestringrequired{  "id": 0,  "name": "string",  "description": "string",  "logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  },  "country": "string",  "currency": {    "iso_currency_code": "string",    "symbol": "string",    "position": "before"  },  "is_marketing_preference_on_customer_forms": true,  "icalendar_links": {    "link": "string",    "webcal_url": "string",    "integrations": [      null    ]  },  "contact_info": {    "email": "string",    "phone_number": "string"  },  "default_registration_settings": {    "registrations_open_interval": "string",    "registrations_close_interval": "string",    "cancellation_notice_interval": "string"  },  "address": {    "street": "string",    "street_secondary": "string",    "city": "string",    "region": "string",    "postal_code": "string",    "country": "string",    "timezone": "string"  }}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [provider]namestringrequiredPossible values: &lt;= 255 charactersdescriptionstringlogo objectnullablerequiredidintegerExample: 13314urlstring&lt;uri&gt;original_widthnumberExample: 64original_heightintegerExample: 64countrystringrequiredcurrency objectrequirediso_currency_codestringrequiredsymbolstringrequiredpositionstringrequired
Possible values: [before, after]is_marketing_preference_on_customer_formsbooleanrequiredicalendar_links object DeferredThis field is DEFERRED.linkstring&lt;uri&gt;requiredwebcal_urlstring&lt;uri&gt;requiredintegrationsundefined[]requiredcontact_info object DeferredThis field is DEFERRED.emailstringnullablerequiredphone_numberstringnullablerequireddefault_registration_settings object DeferredThis field is DEFERRED.registrations_open_intervalstringrequiredregistrations_close_intervalstringrequiredcancellation_notice_intervalstringrequiredaddress object DeferredThis field is DEFERRED.streetstringrequiredstreet_secondarystringnullablerequiredcitystringrequiredregionstringnullablerequiredpostal_codestringrequiredcountrystringrequiredtimezonestringrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;description&gt;string&lt;/description&gt;  &lt;logo&gt;    &lt;id&gt;13314&lt;/id&gt;    &lt;url&gt;string&lt;/url&gt;    &lt;original_width&gt;64&lt;/original_width&gt;    &lt;original_height&gt;64&lt;/original_height&gt;  &lt;/logo&gt;  &lt;country&gt;string&lt;/country&gt;  &lt;currency&gt;    &lt;iso_currency_code&gt;string&lt;/iso_currency_code&gt;    &lt;symbol&gt;string&lt;/symbol&gt;    &lt;position&gt;before&lt;/position&gt;  &lt;/currency&gt;  &lt;is_marketing_preference_on_customer_forms&gt;true&lt;/is_marketing_preference_on_customer_forms&gt;  &lt;icalendar_links&gt;    &lt;link&gt;string&lt;/link&gt;    &lt;webcal_url&gt;string&lt;/webcal_url&gt;    &lt;integrations/&gt;  &lt;/icalendar_links&gt;  &lt;contact_info&gt;    &lt;email&gt;string&lt;/email&gt;    &lt;phone_number&gt;string&lt;/phone_number&gt;  &lt;/contact_info&gt;  &lt;default_registration_settings&gt;    &lt;registrations_open_interval&gt;string&lt;/registrations_open_interval&gt;    &lt;registrations_close_interval&gt;string&lt;/registrations_close_interval&gt;    &lt;cancellation_notice_interval&gt;string&lt;/cancellation_notice_interval&gt;  &lt;/default_registration_settings&gt;  &lt;address&gt;    &lt;street&gt;string&lt;/street&gt;    &lt;street_secondary&gt;string&lt;/street_secondary&gt;    &lt;city&gt;string&lt;/city&gt;    &lt;region&gt;string&lt;/region&gt;    &lt;postal_code&gt;string&lt;/postal_code&gt;    &lt;country&gt;string&lt;/country&gt;    &lt;timezone&gt;string&lt;/timezone&gt;  &lt;/address&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/providers/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousListNextAccount StatusCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "description": "string",  "logo": {    "id": 13314,    "url": "string",    "original_width": 64,    "original_height": 64  }
```

```json
{    "iso_currency_code": "string",    "symbol": "string",    "position": "before"  }
```

```json
{    "link": "string",    "webcal_url": "string",    "integrations": [      null    ]  }
```

```json
{    "email": "string",    "phone_number": "string"  }
```

```json
{    "registrations_open_interval": "string",    "registrations_close_interval": "string",    "cancellation_notice_interval": "string"  }
```

```json
{    "street": "string",    "street_secondary": "string",    "city": "string",    "region": "string",    "postal_code": "string",    "country": "string",    "timezone": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


