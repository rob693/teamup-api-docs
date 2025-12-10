# Endpoints_Crm Workflow Actions Retrieve

**Method:** GET
**URL:** `/api/v2//crm/workflow_actions/`

## Summary
Retrieve | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//crm/workflow_actions/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this crm workflow action.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemaoneOfEmailCustomerActionidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [crm_workflow_action]namestringnullableaction_typestringrequired
Possible values: [email_customer]workflowintegerrequiredconditions object[]requiredArray [oneOfCustomerLabelConditioncondition_typestringrequired
Possible values: [customer_label]operatorstringrequired
Possible values: [equals, not_equals]labelstringrequired]email_template objectrequiredsubjectstringrequiredbodystringrequiredscheduled_delaystringnullablerequired{  "id": 0,  "name": "string",  "action_type": "email_customer",  "workflow": 0,  "conditions": [    {      "condition_type": "customer_label",      "operator": "equals",      "label": "string"    }  ],  "email_template": {    "subject": "string",    "body": "string"  },  "scheduled_delay": "string"}SchemaExample (auto)SchemaoneOfEmailCustomerActionidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [crm_workflow_action]namestringnullableaction_typestringrequired
Possible values: [email_customer]workflowintegerrequiredconditions object[]requiredArray [oneOfCustomerLabelConditioncondition_typestringrequired
Possible values: [customer_label]operatorstringrequired
Possible values: [equals, not_equals]labelstringrequired]email_template objectrequiredsubjectstringrequiredbodystringrequiredscheduled_delaystringnullablerequired&lt;root&gt;  &lt;id&gt;0&lt;/id&gt;  &lt;name&gt;string&lt;/name&gt;  &lt;action_type&gt;email_customer&lt;/action_type&gt;  &lt;workflow&gt;0&lt;/workflow&gt;  &lt;conditions&gt;    &lt;condition_type&gt;customer_label&lt;/condition_type&gt;    &lt;operator&gt;equals&lt;/operator&gt;    &lt;label&gt;string&lt;/label&gt;  &lt;/conditions&gt;  &lt;email_template&gt;    &lt;subject&gt;string&lt;/subject&gt;    &lt;body&gt;string&lt;/body&gt;  &lt;/email_template&gt;  &lt;scheduled_delay&gt;string&lt;/scheduled_delay&gt;&lt;/root&gt;Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientconn = http.client.HTTPSConnection("goteamup.com")payload = ''headers = {  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("GET", "/api/v2/crm/workflow_actions/:id", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersid — pathrequiredShow optional parametersformat — query---jsonxmlTeamUp-Provider-ID — headerTeamup-Request-Mode — header---customerproviderSend API RequestResponseClearClick the Send API Request button above and see the response here!PreviousCreateNextUpdateCompanyHomeContact UsSupportAPI Terms of ServiceConnect with usFacebookInstagramXLinkedInCopyright © 2025 TeamUp, Inc.
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "action_type": "email_customer",  "workflow": 0,  "conditions": [    {      "condition_type": "customer_label",      "operator": "equals",      "label": "string"    }
```

```json
{    "subject": "string",    "body": "string"  }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


