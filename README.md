# StakeDAO Off-chain Registry

This repository serves as a centralized registry for deployed StakeDAO protocol instances across different chains. It provides a single source of truth for protocol deployments and configurations.

## Data Registries

The off-chain registry is composed of two main data sources:

### 1. Address Book

- **Location:** `data/address-book/address-book.json`
- **Purpose:** Contains a comprehensive mapping of all protocol, locker, strategy, and votemarket contract addresses for StakeDAO-related protocols across all supported chains. This includes token addresses, governance, gauge controllers, and more, organized by protocol and chain.
- **Format:**
  - JSON object structured as `{ protocol: { chain: { category: { NAME: ADDRESS, ... }, ... }, ... }, ... }`
  - For detailed structure and address listings, see the [Address Book README](data/address-book/README.md).

### 2. Votemarket Registry

- **Location:** `data/votemarket/votemarkets.json`
- **Purpose:** Tracks all deployed Votemarket platform instances across supported chains, listing the protocol, chainId, platform address, and optional deployment seed.
- **Format:**

```jsonc
{
  "count": "number",
  "data": [
    {
      "protocol": "string",     // Protocol name (e.g., "curve", "balancer", "fxn")
      "chainId": "number",      // Chain ID where instance is deployed
      "platform": "string",     // Contract address of the deployed instance
      "seed": "string | null"   // Deployment seed (if applicable)
    }
  ]
}
```

## Updates

This registry is automatically synchronized with protocol repositories. Manual updates should not be made directly to this repository.

## License

MIT
