# StakeDAO Off-chain Registry

This repository serves as a centralized registry for deployed StakeDAO protocol instances across different chains. It provides a single source of truth for protocol deployments and configurations.

## Registries

### Votemarket Registry
- Location: `data/votemarket/votemarkets.json`
- Purpose: Tracks all deployed Votemarket instances across supported chains
- Format:

```jsonc
{
  "count": number,
  "data": [
    {
      "protocol": string,     // Protocol name (e.g., "curve", "balancer", "fxn")
      "chainId": number,      // Chain ID where instance is deployed
      "platform": string,     // Contract address of the deployed instance
      "seed": string | null   // Deployment seed (if applicable)
    }
  ]
}
```

## Updates

This registry is automatically synchronized with protocol repositories. Manual updates should not be made directly to this repository.

## License

MIT
