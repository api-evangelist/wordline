---
name: wordline-get-account-full-info
description: Retrieve an account and its related owner and guarantor information.
api: openapi/wordline-account-api-openapi.yml
operations:
- retrieveAccount
- retrieveAccountOwner
- retrieveAccountGuarantor
generated: '2026-10-09'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/wordline-account-api-openapi.yml ; every operationId checked against the contract
---

# wordline-get-account-full-info

Retrieve an account and its related owner and guarantor information.

## Steps

1. 1. Call `retrieveAccount` with path parameters `issuerId` and `accountReference`.
2. 2. Call `retrieveAccountOwner` with the same `issuerId` and `accountReference`.
3. 3. Call `retrieveAccountGuarantor` with the same `issuerId` and `accountReference`.

## Rules

- Include an `Authorization` header as defined by the HTTP auth scheme.
- All calls are read‑only; no idempotency key is required.
