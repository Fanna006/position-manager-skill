# CLMM Position Manager Skill.

A quantitative, multi agent execution skill for the **Solana AI Kit**. This tool monitors Concentrated Liquidity Market Maker (CLMM) positions across Orca Whirlpools, Raydium and Meteora. It acts as an automated DeFi quantitative analyst, tracking impermanent loss and simulating optimal rebalances.

## The Problem.
Providing liquidity in CLMMs requires constant mathematical vigilance. When prices move out of bounds, liquidity providers stop earning fees and suffer impermanent loss. Manually tracking tick boundaries and calculating the optimal rebalance ratio is a complex algorithmic process that most founders and users struggle to maintain.

## The Solution.
This skill introduces a specialized analytical agent that ingests current pool price ticks, calculates exact divergence ratios and provides executable rebalance commands to center positions automatically.

## Advanced Repository Architecture
This skill utilizes a multi-layered folder structure to separate analytical context from executable commands, keeping token usage highly efficient:

    position-manager-skill/
    │
    ├── skill/
    │   └── SKILL.md                          # Primary routing hub
    │
    ├── agents/
    │   └── impermanent_loss_agent.md         # Quantitative tick & IL logic
    │
    ├── commands/
    │   └── rebalance.sh                      # Executable CLI rebalance mock
    │
    ├── LICENSE                               # MIT Licensed
    └── README.md                             # You are here

## Installation
To use within your Claude Code / Solana AI Kit workspace:
1. Clone the repository.
2. Move the `skill/`, `agents/` and `commands/` folders into your kit's root structure.
3. Query the agent: *"Analyze my Orca SOL/USDC position and run the impermanent loss agent."*

## License
Licensed under the [MIT License](LICENSE).
