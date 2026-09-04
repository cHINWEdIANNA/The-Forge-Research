# Historical Validation

Historical testing in The Forge is used to decide whether a strategy deserves genuinely unseen forward testing.

A strong full-sample backtest alone is not sufficient. Research also considers chronological out-of-sample performance, drawdown, robustness, execution assumptions, cost sensitivity, and stability across different periods.

---

## V13 — SELL Baseline

V13 emerged as the strongest branch of the original directional research.

### Historical Performance

| Metric | Result |
|---|---:|
| Trades | 150 |
| Wins | 78 |
| Win Rate | 52.0% |
| Net R | +84R |
| Profit Factor | 2.17 |
| Expectancy | +0.56R |
| Max Drawdown | -8R |

### Rolling Out-of-Sample Validation

| Metric | Result |
|---|---:|
| OOS Trades | 104 |
| Net R | +67R |
| Expectancy | +0.644R |
| Positive Windows | 6 / 6 |

The SELL branch materially outperformed the corresponding BUY research.

**Research Decision:** ADVANCE TO FORWARD TESTING

---

## V17 — Filtered SELL

V17 investigates whether a smaller subset of V13 setups can produce higher average trade quality.

The candidate filtering logic was tested chronologically rather than simply selecting attractive completed trades after the fact.

### Rolling OOS Comparison

| Metric | V13 Baseline | V17 Filtered |
|---|---:|---:|
| Trades | 104 | 35 |
| Net R | +67R | +37R |
| Expectancy | +0.644R | +1.057R |
| Positive Windows | 6 / 6 | 5 / 6 |

V17 produced higher historical expectancy but substantially fewer trades.

For that reason, it did **not** replace V13. Both were advanced to forward testing so their behavior could be compared using unseen data.

**Research Decision:** ADVANCE TO FORWARD TESTING

---

## V19 — Independent Trend / Breakout BUY

V19 was developed as an independent BUY-side strategy rather than attempting to repair the weaker ICT-style BUY branch.

### Historical Performance

| Metric | Full Sample | Training | Later / OOS |
|---|---:|---:|---:|
| Trades | 847 | 592 | 255 |
| Win Rate | 28.57% | 28.55% | 28.63% |
| Net R | +121R | +84R | +37R |
| Profit Factor | 1.20 | 1.20 | 1.20 |
| Expectancy | +0.143R | +0.142R | +0.145R |
| Max Drawdown | -29R | -22R | -29R |

Additional validation:

- All 8 chronological equal-trade blocks were profitable.
- Training and later/OOS performance were similar.
- 4 of 5 calendar years were profitable.
- Cost stress remained positive through approximately 0.10R per trade.
- Monte Carlo median maximum drawdown was approximately -30R.
- 95th-percentile Monte Carlo maximum drawdown was approximately -47R.

The historical edge is substantially thinner than V13, making forward execution and drawdown behavior particularly important.

**Research Decision:** ADVANCE TO FORWARD TESTING

---

# Rejected Research

The Forge records failed experiments as well as successful ones.

## ICT-Style BUY

Final executable validation:

| Metric | Result |
|---|---:|
| Trades | 93 |
| Net R | +3R |
| Profit Factor | 1.049 |
| Expectancy | +0.032R |
| Later Sample | -7R |
| Later PF | 0.667 |
| Robustness Checks Passed | 0 / 8 |

**Decision:** SHELVED

---

## Volatility-Compression BUY

The full historical sample remained positive, but the later sample deteriorated.

| Metric | Full | Training | Later |
|---|---:|---:|---:|
| Trades | 563 | 394 | 169 |
| Net R | +53R | +54R | -1R |
| Profit Factor | 1.130 | 1.191 | 0.992 |

**Decision:** SHELVED

---

## Statistical Mean-Reversion BUY

The training-selected configuration failed to maintain its performance in later data.

| Metric | Full | Later |
|---|---:|---:|
| Net R | +47.5R | -11R |
| Profit Factor | 1.111 | 0.926 |

**Decision:** SHELVED

---

# Research Principle

A strategy is not advanced because it can be made profitable somewhere in historical data.

The objective is to find evidence that survives:

1. Chronological separation
2. Out-of-sample testing
3. Realistic execution assumptions
4. Cost stress
5. Drawdown analysis
6. Robustness testing
7. Genuinely unseen forward testing

A failed strategy is considered a useful research result when it prevents the same weak hypothesis from being repeatedly optimized.
