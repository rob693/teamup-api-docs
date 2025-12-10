# Endpoints_Reports Customers Export Export Data

**Method:** GET
**URL:** `/api/v2//reports/customers/export`

## Summary
Data Export | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

POST https://goteamup.com/api/v2//reports/customers/export
Query Parametersformat stringPossible values: [csv, json]
application/jsonapplication/x-www-form-urlencodedmultipart/form-dataBodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Specify which columns to include.Possible values: [id, full_name, first_name, last_name, email, created_at, deleted_at, is_active, date_of_birth, age, phone_number, address, days_until_birthday, gender, is_claimed, is_new, is_slipping_away, registration_blocked, has_failed_payments, has_retry_payments, family_id, family.id, family, family_name, family.name, family_role, family.role, family_managers, family.managers, venue_id, venue.id, venue, venue_name, venue.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, referral_code, thumbnail_url, active_customer_memberships, inactive_customer_memberships, on_hold_customer_memberships, referring_member_id, referring_member.id, referring_member, referrering_member_name, referring_member.name, account_credit_balance, last_payment_at, last_payment_amount, registered_and_attended_count, registrations_count, attendances_count, late_cancels_count, no_shows_count, latest_registration, emergency_contact_name, emergency_contact.name, emergency_contact, emergency_contact_relationship, emergency_contact.relationship, emergency_contact_phone, emergency_contact.phone, lead_source, lead_source.name, is_lead]include_deletedbooleanWhether to include deleted customers in the report.Default value: falsecreated_at_ltestring&lt;date-time&gt;Only return rows for customers that were created on or before a particular timestamp.created_at_gtestring&lt;date-time&gt;Only return rows for customers that were created on or after a particular timestamp.latest_registration_starts_at_ltestring&lt;date-time&gt;Only include customers who latest-registered event occurs on or before this timestamp.latest_registration_starts_at_gtestring&lt;date-time&gt;Only include customers who latest-registered event occurs on or after this timestamp.date_of_birth_ltestring&lt;date&gt;Only return rows for customers with a date of birth on or before this date.date_of_birth_gtestring&lt;date&gt;Only return rows for customers with a date of birth on or after this date.created_at_timeframestringOnly return rows for customers that were created within a particular timeframe. See section on timeframe syntax for formatting.idsinteger[]Only return rows for customers with particular unique identifiers. Format as comma-separated id values.is_newbooleanReturn rows based on whether customers are new or not.is_claimedbooleanReturn rows based on whether customers are claimed or not.is_activebooleanReturn rows based on whether customers are active or not.is_slipping_awaybooleanReturn rows based on whether customers are slipping away or not.is_anystring[]Only include customers who have certain traits.Possible values: [new, claimed, slipping_away, inactive, active, registration_blocked, lead]registration_blockedbooleanhas_account_creditbooleanReturn rows based on whether customers have account credit or not.active_membershipsinteger[]Only return customers who have particular memberships that are active. Format as comma-separated membership id values.extra_customer_fieldsstringSpecify custom fields to include in the report. Format as field id values.Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Specify which columns to include.Possible values: [id, full_name, first_name, last_name, email, created_at, deleted_at, is_active, date_of_birth, age, phone_number, address, days_until_birthday, gender, is_claimed, is_new, is_slipping_away, registration_blocked, has_failed_payments, has_retry_payments, family_id, family.id, family, family_name, family.name, family_role, family.role, family_managers, family.managers, venue_id, venue.id, venue, venue_name, venue.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, referral_code, thumbnail_url, active_customer_memberships, inactive_customer_memberships, on_hold_customer_memberships, referring_member_id, referring_member.id, referring_member, referrering_member_name, referring_member.name, account_credit_balance, last_payment_at, last_payment_amount, registered_and_attended_count, registrations_count, attendances_count, late_cancels_count, no_shows_count, latest_registration, emergency_contact_name, emergency_contact.name, emergency_contact, emergency_contact_relationship, emergency_contact.relationship, emergency_contact_phone, emergency_contact.phone, lead_source, lead_source.name, is_lead]include_deletedbooleanWhether to include deleted customers in the report.Default value: falsecreated_at_ltestring&lt;date-time&gt;Only return rows for customers that were created on or before a particular timestamp.created_at_gtestring&lt;date-time&gt;Only return rows for customers that were created on or after a particular timestamp.latest_registration_starts_at_ltestring&lt;date-time&gt;Only include customers who latest-registered event occurs on or before this timestamp.latest_registration_starts_at_gtestring&lt;date-time&gt;Only include customers who latest-registered event occurs on or after this timestamp.date_of_birth_ltestring&lt;date&gt;Only return rows for customers with a date of birth on or before this date.date_of_birth_gtestring&lt;date&gt;Only return rows for customers with a date of birth on or after this date.created_at_timeframestringOnly return rows for customers that were created within a particular timeframe. See section on timeframe syntax for formatting.idsinteger[]Only return rows for customers with particular unique identifiers. Format as comma-separated id values.is_newbooleanReturn rows based on whether customers are new or not.is_claimedbooleanReturn rows based on whether customers are claimed or not.is_activebooleanReturn rows based on whether customers are active or not.is_slipping_awaybooleanReturn rows based on whether customers are slipping away or not.is_anystring[]Only include customers who have certain traits.Possible values: [new, claimed, slipping_away, inactive, active, registration_blocked, lead]registration_blockedbooleanhas_account_creditbooleanReturn rows based on whether customers have account credit or not.active_membershipsinteger[]Only return customers who have particular memberships that are active. Format as comma-separated membership id values.extra_customer_fieldsstringSpecify custom fields to include in the report. Format as field id values.Bodyid_gtintegersortstring[]The column names to order the returned rows by. Prefix with a - (minus) sign for descending order.Possible values: non-emptyformatstring
Possible values: [csv, json]Default value: csvcolumnsstring[]Specify which columns to include.Possible values: [id, full_name, first_name, last_name, email, created_at, deleted_at, is_active, date_of_birth, age, phone_number, address, days_until_birthday, gender, is_claimed, is_new, is_slipping_away, registration_blocked, has_failed_payments, has_retry_payments, family_id, family.id, family, family_name, family.name, family_role, family.role, family_managers, family.managers, venue_id, venue.id, venue, venue_name, venue.name, instructor_id, instructor.id, instructor, instructor_name, instructor.name, referral_code, thumbnail_url, active_customer_memberships, inactive_customer_memberships, on_hold_customer_memberships, referring_member_id, referring_member.id, referring_member, referrering_member_name, referring_member.name, account_credit_balance, last_payment_at, last_payment_amount, registered_and_attended_count, registrations_count, attendances_count, late_cancels_count, no_shows_count, latest_registration, emergency_contact_name, emergency_contact.name, emergency_contact, emergency_contact_relationship, emergency_contact.relationship, emergency_contact_phone, emergency_contact.phone, lead_source, lead_source.name, is_lead]include_deletedbooleanWhether to include deleted customers in the report.Default value: falsecreated_at_ltestring&lt;date-time&gt;Only return rows for customers that were created on or before a particular timestamp.created_at_gtestring&lt;date-time&gt;Only return rows for customers that were created on or after a particular timestamp.latest_registration_starts_at_ltestring&lt;date-time&gt;Only include customers who latest-registered event occurs on or before this timestamp.latest_registration_starts_at_gtestring&lt;date-time&gt;Only include customers who latest-registered event occurs on or after this timestamp.date_of_birth_ltestring&lt;date&gt;Only return rows for customers with a date of birth on or before this date.date_of_birth_gtestring&lt;date&gt;Only return rows for customers with a date of birth on or after this date.created_at_timeframestringOnly return rows for customers that were created within a particular timeframe. See section on timeframe syntax for formatting.idsinteger[]Only return rows for customers with particular unique identifiers. Format as comma-separated id values.is_newbooleanReturn rows based on whether customers are new or not.is_claimedbooleanReturn rows based on whether customers are claimed or not.is_activebooleanReturn rows based on whether customers are active or not.is_slipping_awaybooleanReturn rows based on whether customers are slipping away or not.is_anystring[]Only include customers who have certain traits.Possible values: [new, claimed, slipping_away, inactive, active, registration_blocked, lead]registration_blockedbooleanhas_account_creditbooleanReturn rows based on whether customers have account credit or not.active_membershipsinteger[]Only return customers who have particular memberships that are active. Format as comma-separated membership id values.extra_customer_fieldsstringSpecify custom fields to include in the report. Format as field id values.
Responses​200application/jsontext/csvSchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}SchemaExample (auto)SchemajobintegerrequiredThe id of a job running asynchronously to generate the report file for download. The job can be retrieved using the GET /jobs/{id} endpoint.{  "job": 0}Authorization: Authorizationname: Authorizationtype: httpscheme: bearerin: headerdescription: Use the prefix `Token ` followed by the token value.pythoncurlphpjavascriptswiftrustrubyHTTP.CLIENTREQUESTSimport http.clientimport jsonconn = http.client.HTTPSConnection("goteamup.com")payload = json.dumps({  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "include_deleted": False,  "created_at_lte": "2024-07-29T15:51:28.071Z",  "created_at_gte": "2024-07-29T15:51:28.071Z",  "latest_registration_starts_at_lte": "2024-07-29T15:51:28.071Z",  "latest_registration_starts_at_gte": "2024-07-29T15:51:28.071Z",  "date_of_birth_lte": "2024-07-29",  "date_of_birth_gte": "2024-07-29",  "created_at_timeframe": "string",  "ids": [    0  ],  "is_new": True,  "is_claimed": True,  "is_active": True,  "is_slipping_away": True,  "is_any": [    "new"  ],  "registration_blocked": True,  "has_account_credit": True,  "active_memberships": [    0  ],  "extra_customer_fields": "string"})headers = {  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}conn.request("POST", "/api/v2/reports/customers/export", payload, headers)res = conn.getresponse()data = res.read()print(data.decode("utf-8"))Request Collapse allBase URLEdithttps://goteamup.com/api/v2AuthSecurity SchemeToken AuthenticationJWT AuthenticationBearer TokenParametersShow optional parametersformat — query---csvjsonBodyContent-Typeapplication/jsonapplication/x-www-form-urlencodedmultipart/form-data{
"id_gt": 0,
"sort": [
"format": "csv",
## Example Request / Response JSON
```json
{id}
```

```json
{  "job": 0}
```

```json
{id}
```

```json
{  "job": 0}
```

```json
{  "id_gt": 0,  "sort": [    "string"  ],  "format": "csv",  "columns": [    "id"  ],  "include_deleted": False,  "created_at_lte": "2024-07-29T15:51:28.071Z",  "created_at_gte": "2024-07-29T15:51:28.071Z",  "latest_registration_starts_at_lte": "2024-07-29T15:51:28.071Z",  "latest_registration_starts_at_gte": "2024-07-29T15:51:28.071Z",  "date_of_birth_lte": "2024-07-29",  "date_of_birth_gte": "2024-07-29",  "created_at_timeframe": "string",  "ids": [    0  ],  "is_new": True,  "is_claimed": True,  "is_active": True,  "is_slipping_away": True,  "is_any": [    "new"  ],  "registration_blocked": True,  "has_account_credit": True,  "active_memberships": [    0  ],  "extra_customer_fields": "string"}
```

```json
{  'Content-Type': 'application/json',  'Accept': 'application/json',  'Authorization': 'Bearer &lt;Authorization&gt;'}
```

```json
{
"id_gt": 0,
"sort": [
"string"
],
"format": "csv",
"columns": [
"id"
],
"include_deleted": false,
"created_at_lte": "2024-07-29T15:51:28.071Z",
"created_at_gte": "2024-07-29T15:51:28.071Z",
"latest_registration_starts_at_lte": "2024-07-29T15:51:28.071Z",
"latest_registration_starts_at_gte": "2024-07-29T15:51:28.071Z",
"date_of_birth_lte": "2024-07-29",
"date_of_birth_gte": "2024-07-29",
"created_at_timeframe": "string",
"ids": [
0
],
"is_new": true,
"is_claimed": true,
"is_active": true,
"is_slipping_away": true,
"is_any": [
"new"
],
"registration_blocked": true,
"has_account_credit": true,
"active_memberships": [
0
],
"extra_customer_fields": "string"
}
```


