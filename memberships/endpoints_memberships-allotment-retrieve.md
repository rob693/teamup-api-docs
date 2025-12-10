# Endpoints_Memberships Allotment Retrieve

**Method:** GET
**URL:** `/api/v2//memberships/`

## Summary
Allotment | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//memberships/:id/allotment
Path Parametersid integerrequiredA unique integer value identifying this membership.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaignore_no_showsbooleanrequiredperiod_limits object[]requiredArray [max_usesintegerrequiredperiodstringrequiredtypestringrequiredoffering_type_limits object[]requiredArray [max_usesintegerrequiredis_extrabooleanrequiredallow_zerobooleanrequiredoffering_type objectrequiredidintegernamestring]]typesstring[]requiredPossible values: [event, course]{  "ignore_no_shows": true,  "period_limits": [    {      "max_uses": 0,      "period": "string",      "type": "string",      "offering_type_limits": [        {          "max_uses": 0,          "is_extra": true,          "allow_zero": true,          "offering_type": {            "id": 0,            "name": "string"          }        }      ]    }  ],  "types": [    "event"  ]}SchemaExample (auto)Schemaignore_no_showsbooleanrequiredperiod_limits object[]requiredArray [max_usesintegerrequiredperiodstringrequiredtypestringrequiredoffering_type_limits object[]requiredArray [max_usesintegerrequiredis_extrabooleanrequiredallow_zerobooleanrequiredoffering_type objectrequiredidintegernamestring]]typesstring[]requiredPossible values: [event, course]&lt;root&gt;  &lt;ignore_no_shows&gt;true&lt;/ignore_no_shows&gt;  &lt;period_limits&gt;    &lt;max_uses&gt;0&lt;/max_uses&gt;    &lt;period&gt;string&lt;/period&gt;    &lt;type&gt;string&lt;/type&gt;    &lt;offering_type_limits&gt;      &lt;max_uses&gt;0&lt;/max_uses&gt;      &lt;is_extra&gt;true&lt;/is_extra&gt;      &lt;allow_zero&gt;true&lt;/allow_zero&gt;      &lt;offering_type&gt;        &lt;id&gt;0&lt;/id&gt;        &lt;name&gt;string&lt;/name&gt;      &lt;/offering_type&gt;    &lt;/offering_type_limits&gt;  &lt;/period_limits&gt;  &lt;types&gt;event&lt;/types&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/memberships/:id/allotment", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousUpdateNextUpdate AllotmentCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "ignore_no_shows": true,  "period_limits": [    {      "max_uses": 0,      "period": "string",      "type": "string",      "offering_type_limits": [        {          "max_uses": 0,          "is_extra": true,          "allow_zero": true,          "offering_type": {            "id": 0,            "name": "string"          }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


