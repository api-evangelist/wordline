---
name: wordline-transaction-dispute
description: Create a dispute for a transaction and retrieve the dispute information.
api: openapi/wordline-transaction-api-openapi.yml
operations:
- retrieveTransactionDetailsByTransactionId
- createDisputeFromTransaction
- getDisputeFolderInfoByTransactionId
generated: '2026-10-09'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/wordline-transaction-api-openapi.yml ; every operationId checked against the contract
---

# wordline-transaction-dispute

Create a dispute for a transaction and retrieve the dispute information.

## Steps

1. 1. `retrieveTransactionDetailsByTransactionId` – requires path parameters `issuerId` and `transactionId` and the `Authorization` header.
2. 2. `createDisputeFromTransaction` – requires path parameters `issuerId` and `transactionId`, the request body with dispute details, and the `Authorization` header.
3. 3. `getDisputeFolderInfoByTransactionId` – requires path parameters `issuerId` and `transactionId` and the `Authorization` header.

## Rules

- Use the `Authorization` HTTP header (Bearer token) for all calls.
- All operations are idempotent when the same `transactionId` and request payload are used.
