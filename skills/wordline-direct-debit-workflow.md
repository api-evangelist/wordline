---
name: wordline-direct-debit-workflow
description: Create, retrieve, and cancel a direct debit instruction.
api: openapi/wordline-direct-debit-api-openapi.yml
operations:
- createDirectDebit
- retrieveDirectDebit
- cancelDirectDebit
generated: '2026-10-09'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/wordline-direct-debit-api-openapi.yml ; every operationId checked against the contract
---

# wordline-direct-debit-workflow

Create, retrieve, and cancel a direct debit instruction.

## Steps

1. 1. `createDirectDebit` – requires the Authorization header and the request body fields defined by the API.
2. 2. `retrieveDirectDebit` – requires the Authorization header and the path parameters issuerId and endToEndId.
3. 3. `cancelDirectDebit` – requires the Authorization header and the path parameters issuerId and endToEndId.

## Rules

- Include an `Authorization` header as specified by the provider's HTTP auth scheme.
