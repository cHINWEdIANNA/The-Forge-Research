# THE FORGE

### A Systematic Trading Research Chronicle

> Forged through hypothesis, evidence, failure, and iteration.

The Forge is an ongoing systematic trading research project focused on developing, testing, rejecting, and forward-validating quantitative trading strategies.

The goal is not to produce attractive backtests. The goal is to identify trading systems capable of surviving chronological validation, realistic execution assumptions, adverse periods, and genuinely unseen market data.

---

##  Research Status

| Strategy | Direction | Research Family | Status |
|---|---|---|---|
| V13 | SELL | Liquidity / Market Structure | 🟢 Forward Testing |
| V17 | SELL | Filtered Market Structure | 🟢 Forward Testing |
| V19 | BUY | Trend / Breakout | 🟡 Awaiting Forward Signals |
| ICT BUY | BUY | Market Structure | 🔴 Shelved |
| Compression BUY | BUY | Volatility Breakout | 🔴 Shelved |
| Mean Reversion BUY | BUY | Statistical Mean Reversion | 🔴 Shelved |
| Order Flow | TBD | Futures / Footprint | 🔵 Research |

---

## Forward Testing

### Current Results

| Strategy | Trades | Win Rate | Net R | PF | Expectancy |
|---|---:|---:|---:|---:|---:|
| V13 SELL | 20 | 55.0% | **+13R** | 2.44 | +0.65R |
| V17 SELL | 8 | 62.5% | **+7R** | 3.33 | +0.875R |
| V19 BUY | 0 | — | 0R | — | — |

These are small forward samples and are **not forecasts of future performance**.

 [View detailed forward-testing results](results/forward-testing.md)

---

## 🧪 Historical Validation

Strategies must earn their way into forward testing.

Research includes:

- Historical backtesting
- Chronological train/OOS separation
- Rolling out-of-sample validation
- Cost stress testing
- Drawdown analysis
- Monte Carlo analysis where appropriate
- Counterfactual execution testing
- Unseen forward testing

 [View historical validation](results/historical-validation.md)

---

## Research Chronicle

The master research document records the complete development history of The Forge:

- Strategy hypotheses
- Historical results
- Failed experiments
- Methodological mistakes and corrections
- Forward-testing results
- Risk research
- Deployment research
- Research decisions
- New strategy branches

 [Open The Forge Research Chronicle v1.1](research/The_Forge_Systematic_Trading_Research_Chronicle_v1.1.docx)

---

##  Research Philosophy

The Forge follows a simple principle:

**A strategy does not survive because we want it to work. It survives because the evidence fails to kill it.**

Strategies entering forward testing are frozen. Short-term performance is recorded rather than used as justification for immediate parameter changes.

Failed hypotheses remain part of the research record.

---

## Current Research Direction

### Futures Order Flow

The next independent research branch investigates centralized futures order-flow information, including:

- Footprint data
- Bid/ask execution
- Delta
- Absorption
- Imbalances
- Volume-at-price
- Liquidity interaction

This branch is being developed independently from the existing V13/V17 methodology.

Potential research markets include **MNQ/NQ** and **MES/ES**.

---

## Source Code

The production strategy implementations and execution infrastructure are maintained privately.

This public repository focuses on the **research process, validation methodology, results, and decision history** rather than publishing deployable trading systems or credentials.

---

##  Disclaimer

The Forge is an independent research and experimentation project.

Nothing in this repository constitutes financial, investment, or trading advice.

Historical backtests, simulations, paper trading, and forward-test results do not guarantee future performance. Trading involves substantial risk of loss.

---

## Repository Structure

```text
the-forge-research/
│
├── README.md
│
├── research/
│   └── The_Forge_Systematic_Trading_Research_Chronicle_v1.1.docx
│
└── results/
    ├── forward-testing.md
    └── historical-validation.md
