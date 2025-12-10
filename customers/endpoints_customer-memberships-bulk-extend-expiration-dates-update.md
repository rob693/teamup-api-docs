# Endpoints_Customer Memberships Bulk Extend Expiration Dates Update

**Method:** PUT
**URL:** `/api/v2//customer_memberships/bulk_extend_expiration_dates`

## Summary
Bulk Extend Expiration Dates | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//customer_memberships/bulk_extend_expiration_dates
Must have one of the following permissions: super_admin, customers.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyrequiredcustomermembership_idsinteger[]daysintegerrequiredPossible values: &gt;= 1 and &lt;= 1000customer_memberships objectproperty name*anyBodyrequiredcustomermembership_idsinteger[]daysintegerrequiredPossible values: &gt;= 1 and &lt;= 1000customer_memberships objectproperty name*anyBodyrequiredcustomermembership_idsinteger[]daysintegerrequiredPossible values: &gt;= 1 and &lt;= 1000customer_memberships objectproperty name*any
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemacustomermembership_idsinteger[]daysintegerrequiredPossible values: &gt;= 1 and &lt;= 1000customer_memberships objectproperty name*any{  "customermembership_ids": [    0  ],  "days": 0,  "customer_memberships": {}}SchemaExample (auto)Schemacustomermembership_idsinteger[]daysintegerrequiredPossible values: &gt;= 1 and &lt;= 1000customer_memberships objectproperty name*any&lt;root&gt;  &lt;customermembership_ids&gt;0&lt;/customermembership_ids&gt;  &lt;days&gt;0&lt;/days&gt;  &lt;customer_memberships/&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customermembership_ids": [    0  ],  "days": 0,  "customer_memberships": {}})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/customer_memberships/bulk_extend_expiration_dates", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customermembership_ids": [
"days": 0,
"customer_memberships": {}
## Example Request / Response JSON
```json
{  "customermembership_ids": [    0  ],  "days": 0,  "customer_memberships": {}
```

```json
{  "customermembership_ids": [    0  ],  "days": 0,  "customer_memberships": {}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"customermembership_ids": [
0
],
"days": 0,
"customer_memberships": {}
```


