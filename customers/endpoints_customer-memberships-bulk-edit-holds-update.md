# Endpoints_Customer Memberships Bulk Edit Holds Update

**Method:** PUT
**URL:** `/api/v2//customer_memberships/bulk_edit_holds`

## Summary
Bulk Edit Holds | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//customer_memberships/bulk_edit_holds
Must have one of the following permissions: super_admin, customers.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodycustomermembership_idsinteger[]customer_memberships objectproperty name*anystart_datestring&lt;date&gt;end_datestring&lt;date&gt;days_to_addintegerPossible values: &gt;= 1 and &lt;= 1000end_immediatelybooleanmake_open_endedbooleanBodycustomermembership_idsinteger[]customer_memberships objectproperty name*anystart_datestring&lt;date&gt;end_datestring&lt;date&gt;days_to_addintegerPossible values: &gt;= 1 and &lt;= 1000end_immediatelybooleanmake_open_endedbooleanBodycustomermembership_idsinteger[]customer_memberships objectproperty name*anystart_datestring&lt;date&gt;end_datestring&lt;date&gt;days_to_addintegerPossible values: &gt;= 1 and &lt;= 1000end_immediatelybooleanmake_open_endedboolean
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemacustomermembership_idsinteger[]customer_memberships objectproperty name*anystart_datestring&lt;date&gt;end_datestring&lt;date&gt;days_to_addintegerPossible values: &gt;= 1 and &lt;= 1000end_immediatelybooleanmake_open_endedboolean{  "customermembership_ids": [    0  ],  "customer_memberships": {},  "start_date": "2024-07-29",  "end_date": "2024-07-29",  "days_to_add": 0,  "end_immediately": true,  "make_open_ended": true}SchemaExample (auto)Schemacustomermembership_idsinteger[]customer_memberships objectproperty name*anystart_datestring&lt;date&gt;end_datestring&lt;date&gt;days_to_addintegerPossible values: &gt;= 1 and &lt;= 1000end_immediatelybooleanmake_open_endedboolean&lt;root&gt;  &lt;customermembership_ids&gt;0&lt;/customermembership_ids&gt;  &lt;customer_memberships/&gt;  &lt;start_date&gt;2024-07-29&lt;/start_date&gt;  &lt;end_date&gt;2024-07-29&lt;/end_date&gt;  &lt;days_to_add&gt;0&lt;/days_to_add&gt;  &lt;end_immediately&gt;true&lt;/end_immediately&gt;  &lt;make_open_ended&gt;true&lt;/make_open_ended&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customermembership_ids": [    0  ],  "customer_memberships": {},  "start_date": "2024-07-29",  "end_date": "2024-07-29",  "days_to_add": 0,  "end_immediately": True,  "make_open_ended": True})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/customer_memberships/bulk_edit_holds", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customermembership_ids": [
"customer_memberships": {},
"start_date": "2024-07-29",
"end_date": "2024-07-29",
"days_to_add": 0,
## Example Request / Response JSON
```json
{  "customermembership_ids": [    0  ],  "customer_memberships": {}
```

```json
{  "customermembership_ids": [    0  ],  "customer_memberships": {}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"customermembership_ids": [
0
],
"customer_memberships": {}
```


