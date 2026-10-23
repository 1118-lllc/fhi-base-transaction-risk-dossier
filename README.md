# FHI Base Transaction Risk Dossier

An x402-paid API for a decision-ready Base transaction-risk report before an agent sends USDC or trades a token.

## What it returns

For a Base recipient address and ERC-20 token address, the API combines public account and contract signals with live DEX liquidity, 24-hour volume, recent activity, and an explainable `REVIEW` or `CAUTION` decision. It never sends transactions, accesses a wallet, or guarantees safety.

## Price and payment

- Price: **0.25 USDC per dossier**
- Network: Base mainnet
- Payment: x402; no API key or subscription
- Payout wallet: `0xccc59b20c89924a11d4633ff7930e3af2f042478`

## Endpoint

`POST https://polished-truth-c514.fhi-llc-1118.workers.dev/api/v1/base-transaction-risk-dossier`

Request body:

```json
{
  "recipientAddress": "0x0000000000000000000000000000000000000000",
  "tokenAddress": "0x4200000000000000000000000000000000000006"
}
```

An unpaid request returns HTTP 402 with the Base USDC x402 payment requirements. An x402-capable client pays and retries the same request.

## Discovery

- Catalog: https://polished-truth-c514.fhi-llc-1118.workers.dev/catalog
- OpenAPI: https://polished-truth-c514.fhi-llc-1118.workers.dev/openapi.json
- x402scan listing: https://www.x402scan.com/server/bacb0668-87f8-4011-8716-a93f388aee20

## Limits

The result reports public, observed evidence only. It is not financial, legal, or security advice.
