# Endpoints_Memberships Create

**Method:** POST
**URL:** `/api/v2//memberships`

## Summary
Create | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//memberships
Must have one of the following permissions: super_admin.
Query Parametersexpand string[]A comma-separated list of fields to expand.fields string[]A comma-separated list of fields to include. Dot-notation can be used to select nested fields.format stringPossible values: [json, xml]Header ParametersTeamUp-Provider-ID stringID of the provider account the API request is for. Required if the access credentials have access to multiple providers.Teamup-Request-Mode stringPossible values: [customer, provider]The authenticated user may have access to both staff and customer profiles. Indicate which mode that request should run in. Customer mode is more limited. Required if the access credentials have access to both modes.
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyoneOfPackWritePrepaidPlanWriteRecurringPlanWritenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
Possible values: [pack]descriptionstringnullablecategoryintegerrequiredfor_salebooleanDefault value: trueallow_repeat_purchasesbooleanrequiredvisible_to_customersbooleanrequiredpurchasable_only_by_providerbooleanrequirednew_customers_onlybooleanrequiredone_time_feestringrequiredExample: 10.99begin_on_first_registrationbooleanDefault value: falsedurationintegerPossible values: &gt;= 1duration_unitstringPossible values: [days, weeks, months]Default value: daysstart_datestring&lt;date&gt;nullableexpiration_datestring&lt;date&gt;nullablenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
Possible values: [prepaid_plan]descriptionstringnullablecategoryintegerrequiredfor_salebooleanDefault value: trueallow_repeat_purchasesbooleanrequiredvisible_to_customersbooleanrequiredpurchasable_only_by_providerbooleanrequirednew_customers_onlybooleanrequiredone_time_feestringrequiredExample: 10.99begin_on_first_registrationbooleanDefault value: falsedurationintegerPossible values: &gt;= 1duration_unitstringPossible values: [days, weeks, months]Default value: daysstart_datestring&lt;date&gt;nullableexpiration_datestring&lt;date&gt;nullableuse_proratebooleanDefault value: falsenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
Possible values: [recurring_plan]descriptionstringnullablecategoryintegerrequiredfor_salebooleanDefault value: trueallow_repeat_purchasesbooleanrequiredvisible_to_customersbooleanrequiredpurchasable_only_by_providerbooleanrequirednew_customers_onlybooleanrequiredBodyoneOfPackWritePrepaidPlanWriteRecurringPlanWritenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
Possible values: [pack]descriptionstringnullablecategoryintegerrequiredfor_salebooleanDefault value: trueallow_repeat_purchasesbooleanrequiredvisible_to_customersbooleanrequiredpurchasable_only_by_providerbooleanrequirednew_customers_onlybooleanrequiredone_time_feestringrequiredExample: 10.99begin_on_first_registrationbooleanDefault value: falsedurationintegerPossible values: &gt;= 1duration_unitstringPossible values: [days, weeks, months]Default value: daysstart_datestring&lt;date&gt;nullableexpiration_datestring&lt;date&gt;nullablenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
Possible values: [prepaid_plan]descriptionstringnullablecategoryintegerrequiredfor_salebooleanDefault value: trueallow_repeat_purchasesbooleanrequiredvisible_to_customersbooleanrequiredpurchasable_only_by_providerbooleanrequirednew_customers_onlybooleanrequiredone_time_feestringrequiredExample: 10.99begin_on_first_registrationbooleanDefault value: falsedurationintegerPossible values: &gt;= 1duration_unitstringPossible values: [days, weeks, months]Default value: daysstart_datestring&lt;date&gt;nullableexpiration_datestring&lt;date&gt;nullableuse_proratebooleanDefault value: falsenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
Possible values: [recurring_plan]descriptionstringnullablecategoryintegerrequiredfor_salebooleanDefault value: trueallow_repeat_purchasesbooleanrequiredvisible_to_customersbooleanrequiredpurchasable_only_by_providerbooleanrequirednew_customers_onlybooleanrequiredBodyoneOfPackWritePrepaidPlanWriteRecurringPlanWritenamestringrequiredPossible values: non-empty and &lt;= 256 characterstypestringThe type of membership to create. Required when creating a new membership. Cannot be altered when updating an existing membership.
## Example Request / Response JSON
```json
{  "id": 0,  "type": "pack",  "name": "string",  "description": "string",  "begin_on_first_registration": true,  "start_date": "2024-07-29",  "expiration_date": "2024-07-29",  "duration": 0,  "duration_unit": "days",  "one_time_fee": {    "decimal": 0,    "string": "£45",    "iso_currency_code": "gbp",    "currency_symbol": "£",    "currency_symbol_position": "before"  }
```

```json
{    "decimal": 0,    "string": "£45",    "iso_currency_code": "gbp",    "currency_symbol": "£",    "currency_symbol_position": "before"  }
```

```json
{    "decimal": 0,    "string": "£45",    "iso_currency_code": "gbp",    "currency_symbol": "£",    "currency_symbol_position": "before"  }
```

```json
{  "name": "string",  "type": "pack",  "description": "string",  "category": 0,  "for_sale": True,  "allow_repeat_purchases": True,  "visible_to_customers": True,  "purchasable_only_by_provider": True,  "new_customers_only": True,  "one_time_fee": "10.99",  "begin_on_first_registration": False,  "duration": 0,  "duration_unit": "days",  "start_date": "2024-07-29",  "expiration_date": "2024-07-29"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"name": "string",
"type": "pack",
"description": "string",
"category": 0,
"for_sale": true,
"allow_repeat_purchases": true,
"visible_to_customers": true,
"purchasable_only_by_provider": true,
"new_customers_only": true,
"one_time_fee": "10.99",
"begin_on_first_registration": false,
"duration": 0,
"duration_unit": "days",
"start_date": "2024-07-29",
"expiration_date": "2024-07-29"
}
```


