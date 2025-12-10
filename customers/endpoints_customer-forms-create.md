# Endpoints_Customer Forms Create

**Method:** POST
**URL:** `/api/v2//customer_forms`

## Summary
Create | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//customer_forms
Must have one of the following permissions: super_admin.
Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequirednamestringrequiredPossible values: non-empty and &lt;= 128 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767offering_types_applies_tostringPossible values: [all, only, all_except, none]offering_typesinteger[]memberships_applies_tostringPossible values: [all, only, all_except, none]membershipsinteger[]submissions_expire_afterstringnullableforce_stale_updatesbooleannullablefieldsinteger[]BodyrequirednamestringrequiredPossible values: non-empty and &lt;= 128 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767offering_types_applies_tostringPossible values: [all, only, all_except, none]offering_typesinteger[]memberships_applies_tostringPossible values: [all, only, all_except, none]membershipsinteger[]submissions_expire_afterstringnullableforce_stale_updatesbooleannullablefieldsinteger[]BodyrequirednamestringrequiredPossible values: non-empty and &lt;= 128 charactersorderintegerPossible values: &gt;= -32768 and &lt;= 32767offering_types_applies_tostringPossible values: [all, only, all_except, none]offering_typesinteger[]memberships_applies_tostringPossible values: [all, only, all_except, none]membershipsinteger[]submissions_expire_afterstringnullableforce_stale_updatesbooleannullablefieldsinteger[]
Responses​201application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequirednamestringrequiredPossible values: &lt;= 128 characterscreated_atstring&lt;date-time&gt;requiredorderintegerPossible values: &gt;= -32768 and &lt;= 32767offering_types_applies_tostringPossible values: [all, only, all_except, none]offering_typesinteger[]memberships_applies_tostringPossible values: [all, only, all_except, none]membershipsinteger[]submissions_expire_afterstringnullableforce_stale_updatesbooleannullablefieldsinteger[]{  "id": 0,  "name": "string",  "created_at": "2024-07-29T15:51:28.071Z",  "order": 0,  "offering_types_applies_to": "all",  "offering_types": [    0  ],  "memberships_applies_to": "all",  "memberships": [    0  ],  "submissions_expire_after": "string",  "force_stale_updates": true,  "fields": [    0  ]}SchemaExample (auto)SchemaidintegerrequirednamestringrequiredPossible values: &lt;= 128 characterscreated_atstring&lt;date-time&gt;requiredorderintegerPossible values: &gt;= -32768 and &lt;= 32767offering_types_applies_tostringPossible values: [all, only, all_except, none]offering_typesinteger[]memberships_applies_tostringPossible values: [all, only, all_except, none]membershipsinteger[]submissions_expire_afterstringnullableforce_stale_updatesbooleannullablefieldsinteger[]&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;created_at&gt;2024-07-29T15:51:28.071Z&lt;/created_at&gt;  &lt;order&gt;0&lt;/order&gt;  &lt;offering_types_applies_to&gt;all&lt;/offering_types_applies_to&gt;  &lt;offering_types&gt;0&lt;/offering_types&gt;  &lt;memberships_applies_to&gt;all&lt;/memberships_applies_to&gt;  &lt;memberships&gt;0&lt;/memberships&gt;  &lt;submissions_expire_after&gt;string&lt;/submissions_expire_after&gt;  &lt;force_stale_updates&gt;true&lt;/force_stale_updates&gt;  &lt;fields&gt;0&lt;/fields&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "name": "string",  "order": 0,  "offering_types_applies_to": "all",  "offering_types": [    0  ],  "memberships_applies_to": "all",  "memberships": [    0  ],  "submissions_expire_after": "string",  "force_stale_updates": True,  "fields": [    0  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/customer_forms", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"name": "string",
"order": 0,
"offering_types_applies_to": "all",
"offering_types": [
"memberships_applies_to": "all",
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "created_at": "2024-07-29T15:51:28.071Z",  "order": 0,  "offering_types_applies_to": "all",  "offering_types": [    0  ],  "memberships_applies_to": "all",  "memberships": [    0  ],  "submissions_expire_after": "string",  "force_stale_updates": true,  "fields": [    0  ]}
```

```json
{  "name": "string",  "order": 0,  "offering_types_applies_to": "all",  "offering_types": [    0  ],  "memberships_applies_to": "all",  "memberships": [    0  ],  "submissions_expire_after": "string",  "force_stale_updates": True,  "fields": [    0  ]}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"order": 0,
"offering_types_applies_to": "all",
"offering_types": [
0
],
"memberships_applies_to": "all",
"memberships": [
0
],
"submissions_expire_after": "string",
"force_stale_updates": true,
"fields": [
0
]
}
```


