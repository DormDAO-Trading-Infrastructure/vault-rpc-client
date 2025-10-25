# DormDAO Vault Client (Python)

This repository contains the **Python-side client** that connects trading strategies to the **DormDAO Vault** on Base.  
It handles everything *before* transactions reach the blockchain:

1. **Strategy Logic** → user strategies define what to trade.
2. **Aggregator Routing** → find the best venue and quote.
3. **Risk Guardrails** → enforce DormDAO risk limits (token whitelist, size caps, slippage, etc.).
4. **Vault RPC** → submit validated orders to the on-chain vault (second barrier).


Folder Setup:

vault-client/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
├── config.json.example
│
├── vault_client/
│   ├── __init__.py
│   ├── main.py
│   ├── config.py
│   ├── models.py
│   ├── oracle.py
│   ├── aggregator.py
│   ├── guards.py
│   ├── rpc.py
│   ├── strategy_interface.py
│   ├── utils.py
│
├── strategies/
│   ├── __init__.py
│   ├── example_momentum.py
│
└── docs/
    ├── architecture.md
    └── api_reference.md
