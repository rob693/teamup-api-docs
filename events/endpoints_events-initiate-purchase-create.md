# Endpoints_Events Initiate Purchase Create

**Method:** POST
**URL:** `/api/v2//events/`

## Summary
Initiate Purchase | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//events/:id/initiate_purchase
Path Parametersid integerrequiredA unique integer value identifying this event.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredreturn_tostring&lt;uri&gt;requiredPossible values: non-empty and &lt;= 2000 characterscustomerintegerrequiredcustomer_membershipintegernullableselect_drop_inbooleanDefault value: falseBodyrequiredreturn_tostring&lt;uri&gt;requiredPossible values: non-empty and &lt;= 2000 characterscustomerintegerrequiredcustomer_membershipintegernullableselect_drop_inbooleanDefault value: falseBodyrequiredreturn_tostring&lt;uri&gt;requiredPossible values: non-empty and &lt;= 2000 characterscustomerintegerrequiredcustomer_membershipintegernullableselect_drop_inbooleanDefault value: false
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemanext_urlstring&lt;uri&gt;requiredexpires_atstring&lt;date-time&gt;required{  "next_url": "string",  "expires_at": "2024-07-29T15:51:28.071Z"}SchemaExample (auto)Schemanext_urlstring&lt;uri&gt;requiredexpires_atstring&lt;date-time&gt;required&lt;root&gt;  &lt;next_url&gt;string&lt;/next_url&gt;  &lt;expires_at&gt;2024-07-29T15:51:28.071Z&lt;/expires_at&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "return_to": "string",  "customer": 0,  "customer_membership": 0,  "select_drop_in": False})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/events/:id/initiate_purchase", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"return_to": "string",
"customer": 0,
"customer_membership": 0,
"select_drop_in": false
## Example Request / Response JSON
```json
{  "next_url": "string",  "expires_at": "2024-07-29T15:51:28.071Z"}
```

```json
{  "return_to": "string",  "customer": 0,  "customer_membership": 0,  "select_drop_in": False}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"return_to": "string",
"customer": 0,
"customer_membership": 0,
"select_drop_in": false
}
```


