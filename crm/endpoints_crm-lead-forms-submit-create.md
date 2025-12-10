# Endpoints_Crm Lead Forms Submit Create

**Method:** POST
**URL:** `/api/v2//crm/lead_forms/`

## Summary
Submit | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//crm/lead_forms/:id/submit
Path Parametersid integerrequiredA unique integer value identifying this lead form.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredfirst_namestringrequiredPossible values: non-emptylast_namestringrequiredPossible values: non-emptyemailstring&lt;email&gt;requiredPossible values: non-emptycustomer_field_values object[]Array [oneOfobjectobjectobjectobjectobject5-item-properties6-item-propertiesobjectobjectobjectvaluestringrequiredPossible values: non-emptyfieldstringThe unique identifier of the field.valuestringrequiredPossible values: non-emptyfieldstringThe unique identifier of the field.valueintegerrequiredfieldstringThe unique identifier of the field.valuestring&lt;decimal&gt;requiredPossible values: Value must match regular expression ^-?\d{0,17}(?:\.\d{0,3})?$fieldstringThe unique identifier of the field.value objectrequiredanswerbooleanrequiredexplanationstringnullableAn additional explanation. Only required sometimes.fieldstringThe unique identifier of the field.value objectrequiredanswerbooleanrequiredexplanationstringnullableAn additional explanation. Only required sometimes.fieldstringThe unique identifier of the field.valuestring&lt;date&gt;requiredA date.fieldstringThe unique identifier of the field.valuestringrequiredThe phone number.Possible values: non-emptyfieldstringThe unique identifier of the field.]Bodyrequiredfirst_namestringrequiredPossible values: non-emptylast_namestringrequiredPossible values: non-emptyemailstring&lt;email&gt;requiredPossible values: non-emptycustomer_field_values object[]Array [oneOfobjectobjectobjectobjectobject5-item-properties6-item-propertiesobjectobjectobjectvaluestringrequiredPossible values: non-emptyfieldstringThe unique identifier of the field.valuestringrequiredPossible values: non-emptyfieldstringThe unique identifier of the field.valueintegerrequiredfieldstringThe unique identifier of the field.valuestring&lt;decimal&gt;requiredPossible values: Value must match regular expression ^-?\d{0,17}(?:\.\d{0,3})?$fieldstringThe unique identifier of the field.value objectrequiredanswerbooleanrequiredexplanationstringnullableAn additional explanation. Only required sometimes.fieldstringThe unique identifier of the field.value objectrequiredanswerbooleanrequiredexplanationstringnullableAn additional explanation. Only required sometimes.fieldstringThe unique identifier of the field.valuestring&lt;date&gt;requiredA date.fieldstringThe unique identifier of the field.valuestringrequiredThe phone number.Possible values: non-emptyfieldstringThe unique identifier of the field.]Bodyrequiredfirst_namestringrequiredPossible values: non-emptylast_namestringrequiredPossible values: non-emptyemailstring&lt;email&gt;requiredPossible values: non-emptycustomer_field_values object[]Array [oneOfobjectobjectobjectobjectobject5-item-properties6-item-propertiesobjectobjectobjectvaluestringrequiredPossible values: non-emptyfieldstringThe unique identifier of the field.valuestringrequiredPossible values: non-emptyfieldstringThe unique identifier of the field.valueintegerrequiredfieldstringThe unique identifier of the field.valuestring&lt;decimal&gt;requiredPossible values: Value must match regular expression ^-?\d{0,17}(?:\.\d{0,3})?$fieldstringThe unique identifier of the field.value objectrequiredanswerbooleanrequiredexplanationstringnullableAn additional explanation. Only required sometimes.fieldstringThe unique identifier of the field.value objectrequiredanswerbooleanrequiredexplanationstringnullableAn additional explanation. Only required sometimes.fieldstringThe unique identifier of the field.valuestring&lt;date&gt;requiredA date.fieldstringThe unique identifier of the field.valuestringrequiredThe phone number.Possible values: non-emptyfieldstringThe unique identifier of the field.]
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemacustomerstringrequiredThe id of the customer created by the submission.{  "customer": "string"}SchemaExample (auto)SchemacustomerstringrequiredThe id of the customer created by the submission.&lt;customer&gt;string&lt;/customer&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "first_name": "string",  "last_name": "string",  "email": "user@example.com",  "customer_field_values": [    {      "value": "string",      "field": "string"    },    {      "value": "string",      "field": "string"    },    {      "value": 0,      "field": "string"    },    {      "value": "string",      "field": "string"    },    {      "value": {        "answer": True,        "explanation": "string"      },      "field": "string"    },    {      "value": "string",      "field": "string"    },    {      "value": [        "string"      ],      "field": "string"    },    {      "value": {        "answer": True,        "explanation": "string"      },      "field": "string"    },    {      "value": "2024-07-29",      "field": "string"    },    {      "value": "string",      "field": "string"    }  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/crm/lead_forms/:id/submit", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"first_name": "string",
"last_name": "string",
"email": "user@example.com",
"customer_field_values": [
"value": "string",
"field": "string"
## Example Request / Response JSON
```json
{0,17}
```

```json
{0,3}
```

```json
{0,17}
```

```json
{0,3}
```

```json
{0,17}
```

```json
{0,3}
```

```json
{  "customer": "string"}
```

```json
{  "first_name": "string",  "last_name": "string",  "email": "user@example.com",  "customer_field_values": [    {      "value": "string",      "field": "string"    }
```

```json
{      "value": "string",      "field": "string"    }
```

```json
{      "value": 0,      "field": "string"    }
```

```json
{      "value": "string",      "field": "string"    }
```

```json
{      "value": {        "answer": True,        "explanation": "string"      }
```

```json
{      "value": "string",      "field": "string"    }
```

```json
{      "value": [        "string"      ],      "field": "string"    }
```

```json
{      "value": {        "answer": True,        "explanation": "string"      }
```

```json
{      "value": "2024-07-29",      "field": "string"    }
```

```json
{      "value": "string",      "field": "string"    }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"first_name": "string",
"last_name": "string",
"email": "user@example.com",
"customer_field_values": [
{
"value": "string",
"field": "string"
}
```

```json
{
"value": "string",
"field": "string"
}
```

```json
{
"value": 0,
"field": "string"
}
```

```json
{
"value": "string",
"field": "string"
}
```

```json
{
"value": {
"answer": true,
"explanation": "string"
}
```

```json
{
"value": "string",
"field": "string"
}
```

```json
{
"value": [
"string"
],
"field": "string"
}
```

```json
{
"value": {
"answer": true,
"explanation": "string"
}
```

```json
{
"value": "2024-07-29",
"field": "string"
}
```

```json
{
"value": "string",
"field": "string"
}
```


