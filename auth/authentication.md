# Authentication

**Method:** GET
**URL:** `/unknown-endpoint`

## Summary
Authentication | TeamUp Developers

## Request Parameters
(Heuristically extracted. Refine as needed.)

Common use cases:
Common use cases:
Bearer token example:
Authorization: Bearer &lt;TOKEN&gt;
For example, the GET /customers endpoint specifies:
Sometimes, the same person may be both a customer and a staff member. To clarify which mode your request should operate in, include the following header:
TeamUp-Request-Mode: provider
TeamUp-Request-Mode: customer
For franchises or multi-location businesses, your API key may be linked to multiple providers. Use this header to specify which one the request should act on:
TeamUp-Provider-ID: 123

