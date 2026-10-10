---
name: wordline-payment-initiation-flow
description: Initiate a payment, identify and authorise it, confirm the request and retrieve its status.
api: openapi/wordline-payment-initiation-service-api-openapi.yml
operations:
- paymentInitiate
- paymentIdentification
- paymentAuthorisation
- paymentConfirmation
- paymentStatus
generated: '2026-10-09'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/wordline-payment-initiation-service-api-openapi.yml ; every operationId checked against the contract
---

# wordline-payment-initiation-flow

Initiate a payment, identify and authorise it, confirm the request and retrieve its status.

## Steps

1. 1. Call `paymentInitiate` with the required request body fields (e.g., amount, creditor, debtor).
2. 2. Call `paymentIdentification` with the `paymentId` path parameter and identification details.
3. 3. Call `paymentAuthorisation` with the `paymentId` path parameter and authorisation data.
4. 4. Call `paymentConfirmation` with the `paymentId` path parameter to confirm the payment request.
5. 5. Call `paymentStatus` with the `paymentId` path parameter to retrieve the final status.

## Rules

- Include an `Authorization` header with a valid bearer token for each request.
- Use idempotency keys where supported (e.g., `Idempotency-Key` header) for POST operations to avoid duplicate processing.
