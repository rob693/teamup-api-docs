# Endpoints_Crm Workflow Actions List

**Method:** GET
**URL:** `/api/v2//crm/workflow_actions`

## Summary
List | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

GET https://goteamup.com/api/v2//crm/workflow_actions
Must have one of the following permissions: super_admin.
Query Parametersaction_type stringPossible values: [email_customer]
format stringPossible values: [json, xml]page integerA page number within the paginated result set.page_size integerPossible values: &lt;= 100Number of results to return per page.workflow_trigger stringPossible values: [lead_form.submitted]
Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
Responses​200application/jsonapplication/xmlSchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [oneOfEmailCustomerActionidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [crm_workflow_action]namestringnullableaction_typestringrequired
Possible values: [email_customer]workflowintegerrequiredconditions object[]requiredArray [oneOfCustomerLabelConditioncondition_typestringrequired
Possible values: [customer_label]operatorstringrequired
Possible values: [equals, not_equals]labelstringrequired]email_template objectrequiredsubjectstringrequiredbodystringrequiredscheduled_delaystringnullablerequired]{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "name": "string",      "action_type": "email_customer",      "workflow": 0,      "conditions": [        {          "condition_type": "customer_label",          "operator": "equals",          "label": "string"        }      ],      "email_template": {        "subject": "string",        "body": "string"      },      "scheduled_delay": "string"    }  ]}SchemaExample (auto)SchemacountintegerExample: 123nextstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=4previousstring&lt;uri&gt;nullableExample: http://api.example.org/accounts/?page=2results object[]Array [oneOfEmailCustomerActionidintegerrequiredobjectrequiredString representing the object's type. Objects of the same type share the same value.Possible values: [crm_workflow_action]namestringnullableaction_typestringrequired
Possible values: [email_customer]workflowintegerrequiredconditions object[]requiredArray [oneOfCustomerLabelConditioncondition_typestringrequired
## Example Request / Response JSON
```json
{  "count": 123,  "next": "http://api.example.org/accounts/?page=4",  "previous": "http://api.example.org/accounts/?page=2",  "results": [    {      "id": 0,      "name": "string",      "action_type": "email_customer",      "workflow": 0,      "conditions": [        {          "condition_type": "customer_label",          "operator": "equals",          "label": "string"        }
```

```json
{        "subject": "string",        "body": "string"      }
```

```json
{  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```


