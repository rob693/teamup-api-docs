# Endpoints_Auth Check Account Retrieve

**Method:** GET
**URL:** `/api/v2//auth/check_account`

## Summary
Check Account | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//auth/check_account
Query Parametersemail emailrequiredPossible values: non-emptyformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)Schemaaccount_existsbooleanhas_identity_accountbooleanis_claimedbooleanis_hiddenbooleanweb_auth_urlstring{  "account_exists": true,  "has_identity_account": true,  "is_claimed": true,  "is_hidden": true,  "web_auth_url": "string"}SchemaExample (auto)Schemaaccount_existsbooleanhas_identity_accountbooleanis_claimedbooleanis_hiddenbooleanweb_auth_urlstring&lt;root&gt;  &lt;account_exists&gt;true&lt;/account_exists&gt;  &lt;has_identity_account&gt;true&lt;/has_identity_account&gt;  &lt;is_claimed&gt;true&lt;/is_claimed&gt;  &lt;is_hidden&gt;true&lt;/is_hidden&gt;  &lt;web_auth_url&gt;string&lt;/web_auth_url&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/auth/check_account", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersemail — queryrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousAuthenticated ApplicationNextPassword LoginCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "account_exists": true,  "has_identity_account": true,  "is_claimed": true,  "is_hidden": true,  "web_auth_url": "string"}
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


