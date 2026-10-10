---
name: wordline-create-and-retrieve-customer
description: Create a new customer and then retrieve its details.
api: openapi/wordline-customer-api-openapi.yml
operations:
- createCustomer
- retrieveCustomer
generated: '2026-10-09'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/wordline-customer-api-openapi.yml ; every operationId checked against the contract
---

# wordline-create-and-retrieve-customer

Create a new customer and then retrieve its details.

## Steps

1. 1. Call `createCustomer` with the required request body fields for the new customer.
2. 2. Call `retrieveCustomer` with the `customerReference` returned from the creation step.

## Rules

- Include the `Authorization` header as defined by the provider's HTTP auth scheme.
- Use the appropriate server base URL, e.g., `https://sbx-wlip.api1-eu2.psapigateway.preprod.giservices.io/card-issuing/api/v2`.
