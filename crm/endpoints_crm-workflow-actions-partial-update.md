# Endpoints_Crm Workflow Actions Partial Update

**Method:** PATCH
**URL:** `/api/v2//crm/workflow_actions/`

## Summary
Partially Update | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

PATCH https://goteamup.com/api/v2//crm/workflow_actions/:id
Must have one of the following permissions: super_admin.
Path Parametersid integerrequiredA unique integer value identifying this crm workflow action.Query Parametersformat stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyoneOfEmailCustomerActionnamestringnullablePossible values: non-emptyaction_typestringrequired
Possible values: [email_customer]workflowintegerrequiredconditions object[]requiredArray [oneOfCustomerLabelConditioncondition_typestringrequired
Possible values: [customer_label]operatorstringrequired
Possible values: [equals, not_equals]labelstringrequiredPossible values: non-empty]email_template objectrequiredsubjectstringrequiredPossible values: non-emptybodystringrequiredPossible values: non-emptyscheduled_delaystringnullablerequiredBodyoneOfEmailCustomerActionnamestringnullablePossible values: non-emptyaction_typestringrequired
Possible values: [email_customer]workflowintegerrequiredconditions object[]requiredArray [oneOfCustomerLabelConditioncondition_typestringrequired
Possible values: [customer_label]operatorstringrequired
Possible values: [equals, not_equals]labelstringrequiredPossible values: non-empty]email_template objectrequiredsubjectstringrequiredPossible values: non-emptybodystringrequiredPossible values: non-emptyscheduled_delaystringnullablerequiredBodyoneOfEmailCustomerActionnamestringnullablePossible values: non-emptyaction_typestringrequired
## Example Request / Response JSON
```json
{  "id": 0,  "name": "string",  "action_type": "email_customer",  "workflow": 0,  "conditions": [    {      "condition_type": "customer_label",      "operator": "equals",      "label": "string"    }
```

```json
{    "subject": "string",    "body": "string"  }
```

```json
{  "name": "string",  "action_type": "email_customer",  "workflow": 0,  "conditions": [    {      "condition_type": "customer_label",      "operator": "equals",      "label": "string"    }
```

```json
{    "subject": "string",    "body": "string"  }
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"action_type": "email_customer",
"workflow": 0,
"conditions": [
{
"condition_type": "customer_label",
"operator": "equals",
"label": "string"
}
```

```json
{
"subject": "string",
"body": "string"
}
```


