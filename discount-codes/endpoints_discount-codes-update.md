# Endpoints_Discount Codes Update

**Method:** PUT
**URL:** `/api/v2//discount_codes/`

## Summary
Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//discount_codes/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this discount code.Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequirednamestringrequiredPossible values: non-empty and &lt;= 100 charactersallowed_usesintegernullablerequiredallowed_uses_per_customerintegernullablerequireddiscount_typestringrequiredPossible values: [flat, percent]discount_amountstring&lt;decimal&gt;requiredPossible values: Value must match regular expression ^-?\d{0,5}(?:\.\d{0,2})?$usable_start_datestring&lt;date&gt;nullableusable_end_datestring&lt;date&gt;nullableusable_purchase_typesstring[]requiredPossible values: [event, course, membership, store, joining_fee]usable_by_new_customers_onlybooleanrequiredusable_by_default_for_purchase_typesbooleanrequiredapplicable_billing_cyclesintegerrequiredstatusstringPossible values: [inactive, active]Default value: activeBodyrequirednamestringrequiredPossible values: non-empty and &lt;= 100 charactersallowed_usesintegernullablerequiredallowed_uses_per_customerintegernullablerequireddiscount_typestringrequiredPossible values: [flat, percent]discount_amountstring&lt;decimal&gt;requiredPossible values: Value must match regular expression ^-?\d{0,5}(?:\.\d{0,2})?$usable_start_datestring&lt;date&gt;nullableusable_end_datestring&lt;date&gt;nullableusable_purchase_typesstring[]requiredPossible values: [event, course, membership, store, joining_fee]usable_by_new_customers_onlybooleanrequiredusable_by_default_for_purchase_typesbooleanrequiredapplicable_billing_cyclesintegerrequiredstatusstringPossible values: [inactive, active]Default value: activeBodyrequirednamestringrequiredPossible values: non-empty and &lt;= 100 charactersallowed_usesintegernullablerequiredallowed_uses_per_customerintegernullablerequireddiscount_typestringrequiredPossible values: [flat, percent]discount_amountstring&lt;decimal&gt;requiredPossible values: Value must match regular expression ^-?\d{0,5}(?:\.\d{0,2})?$usable_start_datestring&lt;date&gt;nullableusable_end_datestring&lt;date&gt;nullableusable_purchase_typesstring[]requiredPossible values: [event, course, membership, store, joining_fee]usable_by_new_customers_onlybooleanrequiredusable_by_default_for_purchase_typesbooleanrequiredapplicable_billing_cyclesintegerrequiredstatusstringPossible values: [inactive, active]Default value: active
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [discount_code]namestringrequiredPossible values: &lt;= 100 characterscodestringrequiredPossible values: &lt;= 20 charactersstatusstringPossible values: [inactive, active]Default value: activeusesintegerrequiredallowed_usesintegerrequiredallowed_uses_per_customerintegerrequireddiscount_typestringrequiredPossible values: [flat, percent]discount_amount objectrequiredoneOfobjectnumberobjectnumberusable_start_datestring&lt;date&gt;requiredusable_end_datestring&lt;date&gt;requiredusable_purchase_typesstring[]requiredPossible values: [event, course, membership, store, joining_fee]usable_by_new_customers_onlybooleanrequiredusable_by_default_for_purchase_typesbooleanrequiredapplicable_billing_cyclesintegerrequiredgroup objectrequiredidintegerrequirednamestringrequiredPossible values: &lt;= 100 characters{  "id": 0,  "name": "string",  "code": "string",  "status": "active",  "uses": 0,  "allowed_uses": 0,  "allowed_uses_per_customer": 0,  "discount_type": "flat",  "discount_amount": {},  "usable_start_date": "2024-07-29",  "usable_end_date": "2024-07-29",  "usable_purchase_types": [    "event"  ],  "usable_by_new_customers_only": true,  "usable_by_default_for_purchase_types": true,  "applicable_billing_cycles": 0,  "group": {    "id": 0,    "name": "string"  }}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [discount_code]namestringrequiredPossible values: &lt;= 100 characterscodestringrequiredPossible values: &lt;= 20 charactersstatusstringPossible values: [inactive, active]Default value: activeusesintegerrequiredallowed_usesintegerrequiredallowed_uses_per_customerintegerrequireddiscount_typestringrequiredPossible values: [flat, percent]discount_amount objectrequiredoneOfobjectnumberobjectnumberusable_start_datestring&lt;date&gt;requiredusable_end_datestring&lt;date&gt;requiredusable_purchase_typesstring[]requiredPossible values: [event, course, membership, store, joining_fee]usable_by_new_customers_onlybooleanrequiredusable_by_default_for_purchase_typesbooleanrequiredapplicable_billing_cyclesintegerrequiredgroup objectrequiredidintegerrequirednamestringrequiredPossible values: &lt;= 100 characters&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;code&gt;string&lt;/code&gt;  &lt;status&gt;active&lt;/status&gt;  &lt;uses&gt;0&lt;/uses&gt;  &lt;allowed_uses&gt;0&lt;/allowed_uses&gt;  &lt;allowed_uses_per_customer&gt;0&lt;/allowed_uses_per_customer&gt;  &lt;discount_type&gt;flat&lt;/discount_type&gt;  &lt;discount_amount/&gt;  &lt;usable_start_date&gt;2024-07-29&lt;/usable_start_date&gt;  &lt;usable_end_date&gt;2024-07-29&lt;/usable_end_date&gt;  &lt;usable_purchase_types&gt;event&lt;/usable_purchase_types&gt;  &lt;usable_by_new_customers_only&gt;true&lt;/usable_by_new_customers_only&gt;  &lt;usable_by_default_for_purchase_types&gt;true&lt;/usable_by_default_for_purchase_types&gt;  &lt;applicable_billing_cycles&gt;0&lt;/applicable_billing_cycles&gt;  &lt;group&gt;    &lt;id&gt;0&lt;/id&gt;    &lt;name&gt;string&lt;/name&gt;  &lt;/group&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "name": "string",  "allowed_uses": 0,  "allowed_uses_per_customer": 0,  "discount_type": "flat",  "discount_amount": "string",  "usable_start_date": "2024-07-29",  "usable_end_date": "2024-07-29",  "usable_purchase_types": [    "event"  ],  "usable_by_new_customers_only": True,  "usable_by_default_for_purchase_types": True,  "applicable_billing_cycles": 0,  "status": "active"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/discount_codes/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersexpand — queryAdd itemfields — queryAdd itemformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"name": "string",
"allowed_uses": 0,
"allowed_uses_per_customer": 0,
"discount_type": "flat",
"discount_amount": "string",
## Example Request / Response JSON
```json
{0,5}
```

```json
{0,2}
```

```json
{0,5}
```

```json
{0,2}
```

```json
{0,5}
```

```json
{0,2}
```

```json
{  "id": 0,  "name": "string",  "code": "string",  "status": "active",  "uses": 0,  "allowed_uses": 0,  "allowed_uses_per_customer": 0,  "discount_type": "flat",  "discount_amount": {}
```

```json
{    "id": 0,    "name": "string"  }
```

```json
{  "name": "string",  "allowed_uses": 0,  "allowed_uses_per_customer": 0,  "discount_type": "flat",  "discount_amount": "string",  "usable_start_date": "2024-07-29",  "usable_end_date": "2024-07-29",  "usable_purchase_types": [    "event"  ],  "usable_by_new_customers_only": True,  "usable_by_default_for_purchase_types": True,  "applicable_billing_cycles": 0,  "status": "active"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"allowed_uses": 0,
"allowed_uses_per_customer": 0,
"discount_type": "flat",
"discount_amount": "string",
"usable_start_date": "2024-07-29",
"usable_end_date": "2024-07-29",
"usable_purchase_types": [
"event"
],
"usable_by_new_customers_only": true,
"usable_by_default_for_purchase_types": true,
"applicable_billing_cycles": 0,
"status": "active"
}
```


