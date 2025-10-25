# DormDAO Vault Client (Python)

This repository contains the **Python-side client** that connects trading strategies to the **DormDAO Vault** on Base.  
It handles everything *before* transactions reach the blockchain:

1. **Strategy Logic** → user strategies define what to trade.
2. **Aggregator Routing** → find the best venue and quote.
3. **Risk Guardrails** → enforce DormDAO risk limits (token whitelist, size caps, slippage, etc.).
4. **Vault RPC** → submit validated orders to the on-chain vault (second barrier).
