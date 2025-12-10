# Endpoints_Checkins Create

**Method:** POST
**URL:** `/api/v2//checkins`

## Summary
checkins_create | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//checkins
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequireddatestring&lt;date&gt;requiredvenueintegerrequiredcustomerintegerrequiredcustomer_membershipintegercompedbooleanDefault value: falseBodyrequireddatestring&lt;date&gt;requiredvenueintegerrequiredcustomerintegerrequiredcustomer_membershipintegercompedbooleanDefault value: falseBodyrequireddatestring&lt;date&gt;requiredvenueintegerrequiredcustomerintegerrequiredcustomer_membershipintegercompedbooleanDefault value: false
Responses​201application/jsonapplication/xmlSchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [checkin]timestampstring&lt;date-time&gt;requiredcompedbooleanrequiredcustomer_membershipintegerrequired{  "id": 0,  "timestamp": "2024-07-29T15:51:28.071Z",  "comped": true,  "customer_membership": 0}SchemaExample (auto)SchemaidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [checkin]timestampstring&lt;date-time&gt;requiredcompedbooleanrequiredcustomer_membershipintegerrequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;timestamp&gt;2024-07-29T15:51:28.071Z&lt;/timestamp&gt;  &lt;comped&gt;true&lt;/comped&gt;  &lt;customer_membership&gt;0&lt;/customer_membership&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "date": "2024-07-29",  "venue": 0,  "customer": 0,  "customer_membership": 0,  "comped": False})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/checkins", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"date": "2024-07-29",
"venue": 0,
"customer": 0,
"customer_membership": 0,
"comped": false
## Example Request / Response JSON
```json
{  "id": 0,  "timestamp": "2024-07-29T15:51:28.071Z",  "comped": true,  "customer_membership": 0}
```

```json
{  "date": "2024-07-29",  "venue": 0,  "customer": 0,  "customer_membership": 0,  "comped": False}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"date": "2024-07-29",
"venue": 0,
"customer": 0,
"customer_membership": 0,
"comped": false
}
```


