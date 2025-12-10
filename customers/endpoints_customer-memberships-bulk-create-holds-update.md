# Endpoints_Customer Memberships Bulk Create Holds Update

**Method:** PUT
**URL:** `/api/v2//customer_memberships/bulk_create_holds`

## Summary
Bulk Create Holds | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PUT https://goteamup.com/api/v2//customer_memberships/bulk_create_holds
Must have one of the following permissions: super_admin, customers.
Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Possible values: [open_ended, finite]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;disable_proratesbooleanextend_expirationsbooleanBodyrequiredcustomermembership_idsinteger[]customer_memberships objectproperty name*anyhold_typestringrequired
Possible values: [open_ended, finite]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;disable_proratesbooleanextend_expirationsbooleanBodyrequiredcustomermembership_idsinteger[]customer_memberships objectproperty name*anyhold_typestringrequired
Possible values: [open_ended, finite]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;disable_proratesbooleanextend_expirationsboolean
Possible values: [open_ended, finite]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;disable_proratesbooleanextend_expirationsboolean{  "customermembership_ids": [    0  ],  "customer_memberships": {},  "hold_type": "open_ended",  "start_date": "2024-07-29",  "end_date": "2024-07-29",  "disable_prorates": true,  "extend_expirations": true}SchemaExample (auto)Schemacustomermembership_idsinteger[]customer_memberships objectproperty name*anyhold_typestringrequired
Possible values: [open_ended, finite]start_datestring&lt;date&gt;requiredend_datestring&lt;date&gt;disable_proratesbooleanextend_expirationsboolean&lt;root&gt;  &lt;customermembership_ids&gt;0&lt;/customermembership_ids&gt;  &lt;customer_memberships/&gt;  &lt;hold_type&gt;open_ended&lt;/hold_type&gt;  &lt;start_date&gt;2024-07-29&lt;/start_date&gt;  &lt;end_date&gt;2024-07-29&lt;/end_date&gt;  &lt;disable_prorates&gt;true&lt;/disable_prorates&gt;  &lt;extend_expirations&gt;true&lt;/extend_expirations&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "customermembership_ids": [    0  ],  "customer_memberships": {},  "hold_type": "open_ended",  "start_date": "2024-07-29",  "end_date": "2024-07-29",  "disable_prorates": True,  "extend_expirations": True})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("PUT", "/api/v2/customer_memberships/bulk_create_holds", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderBody&nbsp;requiredContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"customermembership_ids": [
"customer_memberships": {},
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


