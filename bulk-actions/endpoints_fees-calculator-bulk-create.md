# Endpoints_Fees Calculator Bulk Create

**Method:** POST
**URL:** `/api/v2//fees_calculator/bulk`

## Summary
Bulk Calculate Fees | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//fees_calculator/bulk
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequireditems object[]requiredPossible values: &gt;= 1, &lt;= 100Array [pre_tax_pricestringExample: 10.99post_tax_pricestringExample: 10.99purchase_typestringrequired
Possible values: [event, course, membership, recurring_membership, store, gift_card, joining_fee]]Bodyrequireditems object[]requiredPossible values: &gt;= 1, &lt;= 100Array [pre_tax_pricestringExample: 10.99post_tax_pricestringExample: 10.99purchase_typestringrequired
Possible values: [event, course, membership, recurring_membership, store, gift_card, joining_fee]]Bodyrequireditems object[]requiredPossible values: &gt;= 1, &lt;= 100Array [pre_tax_pricestringExample: 10.99post_tax_pricestringExample: 10.99purchase_typestringrequired
Possible values: [event, course, membership, recurring_membership, store, gift_card, joining_fee]]
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaresults object[]requiredArray [pre_tax_price objectrequireddecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]post_tax_price objectrequireddecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]fee_line_items object[]requiredArray [amount objectrequireddecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]descriptionstringrequired]]{  "results": [    {      "pre_tax_price": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "post_tax_price": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      },      "fee_line_items": [        {          "amount": {            "decimal": 0,            "string": "£45",            "iso_currency_code": "gbp",            "currency_symbol": "£",            "currency_symbol_position": "before"          },          "description": "string"        }      ]    }  ]}SchemaExample (auto)Schemaresults object[]requiredArray [pre_tax_price objectrequireddecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]post_tax_price objectrequireddecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]fee_line_items object[]requiredArray [amount objectrequireddecimalnumberstringstringThe price as a string.Possible values: non-emptyExample: £45iso_currency_codestringPossible values: non-emptyExample: gbpcurrency_symbolstringPossible values: non-emptyExample: £currency_symbol_positionstringPossible values: non-empty, [before, after]descriptionstringrequired]]&lt;results&gt;  &lt;pre_tax_price&gt;    &lt;decimal&gt;0&lt;/decimal&gt;    &lt;string&gt;£45&lt;/string&gt;    &lt;iso_currency_code&gt;gbp&lt;/iso_currency_code&gt;    &lt;currency_symbol&gt;£&lt;/currency_symbol&gt;    &lt;currency_symbol_position&gt;before&lt;/currency_symbol_position&gt;  &lt;/pre_tax_price&gt;  &lt;post_tax_price&gt;    &lt;decimal&gt;0&lt;/decimal&gt;    &lt;string&gt;£45&lt;/string&gt;    &lt;iso_currency_code&gt;gbp&lt;/iso_currency_code&gt;    &lt;currency_symbol&gt;£&lt;/currency_symbol&gt;    &lt;currency_symbol_position&gt;before&lt;/currency_symbol_position&gt;  &lt;/post_tax_price&gt;  &lt;fee_line_items&gt;    &lt;amount&gt;      &lt;decimal&gt;0&lt;/decimal&gt;      &lt;string&gt;£45&lt;/string&gt;      &lt;iso_currency_code&gt;gbp&lt;/iso_currency_code&gt;      &lt;currency_symbol&gt;£&lt;/currency_symbol&gt;      &lt;currency_symbol_position&gt;before&lt;/currency_symbol_position&gt;    &lt;/amount&gt;    &lt;description&gt;string&lt;/description&gt;  &lt;/fee_line_items&gt;&lt;/results&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "items": [    {      "pre_tax_price": "10.99",      "post_tax_price": "10.99",      "purchase_type": "event"    }  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/fees_calculator/bulk", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"items": [
"pre_tax_price": "10.99",
"post_tax_price": "10.99",
## Example Request / Response JSON
```json
{  "results": [    {      "pre_tax_price": {        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{        "decimal": 0,        "string": "£45",        "iso_currency_code": "gbp",        "currency_symbol": "£",        "currency_symbol_position": "before"      }
```

```json
{          "amount": {            "decimal": 0,            "string": "£45",            "iso_currency_code": "gbp",            "currency_symbol": "£",            "currency_symbol_position": "before"          }
```

```json
{  "items": [    {      "pre_tax_price": "10.99",      "post_tax_price": "10.99",      "purchase_type": "event"    }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"items": [
{
"pre_tax_price": "10.99",
"post_tax_price": "10.99",
"purchase_type": "event"
}
```


