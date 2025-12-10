# Endpoints_Customer Forms Ordering Partial Update

**Method:** PATCH
**URL:** `/api/v2//customer_forms/ordering`

## Summary
Change Customer Form Order | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//customer_forms/ordering
Must have one of the following permissions: super_admin.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyorderinginteger[]Possible values: &gt;= 2Bodyorderinginteger[]Possible values: &gt;= 2Bodyorderinginteger[]Possible values: &gt;= 2
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemastatusstringrequiredConstant value: OKPossible values: [OK]detailstringnullablerequired{  "status": "OK",  "detail": "string"}SchemaExample (auto)SchemastatusstringrequiredConstant value: OKPossible values: [OK]detailstringnullablerequired&lt;root&gt;  &lt;status&gt;OK&lt;/status&gt;  &lt;detail&gt;string&lt;/detail&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "ordering": [    0  ]})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PATCH", "/api/v2/customer_forms/ordering", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"ordering": [
## Example Request / Response JSON
```json
{  "status": "OK",  "detail": "string"}
```

```json
{  "ordering": [    0  ]}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"ordering": [
0
]
}
```


