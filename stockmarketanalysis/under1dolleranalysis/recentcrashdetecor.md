# UNDER-$1 STOCK CRASH DETECTOR

Act as a quantitative equity analyst specializing in micro-cap and penny-stock price movements.

Use the stock universe supplied from the previous research stage.

Do not search for unrelated companies.

## 1. Identify declining stocks

Screen the universe using:

| Period | Decline threshold |
|---|---:|
| 1 day | -10% |
| 5 trading days | -15% |
| 10 trading days | -20% |
| 1 month | -30% |
| 3 months | -40% |
| 6 months | -50% |
| From 52-week high | -60% |

Include every company meeting at least one criterion.

Clearly separate each category.

## 2. Calculate price performance

For each company collect:
- Current price.
- Previous closing price.
- 5-day change.
- 10-day change.
- 1-month change.
- 3-month change.
- 6-month change.
- 52-week change.
- Percentage below 52-week high.
- Percentage above 52-week low.

Use split-adjusted prices.

Do not confuse a decline from an all-time high with a recent crash.

## 3. Investigate trading activity

Analyze:
- 20-day average volume.
- Recent trading volume.
- Relative volume.
- Dollar volume.
- Bid-ask spread, if available.
- Short interest.
- Float.

Identify stocks experiencing unusually high selling volume.

## 4. Classify decline types

A. Sudden crash – Sharp decline within days.

B. Recent correction – Significant decline within one month.

C. Extended decline – Downward trend over several months.

D. Long-term collapse – Severe decline from previous highs.

E. Low-liquidity decline – Price movement potentially distorted by thin trading.

## 5. Final output

| Company | Ticker | Price | 1W | 1M | 3M | 6M | From high | Relative volume | Decline type |

Sort by the most severe recent decline.

Provide the exact data date and sources.

FINAL OBJECTIVE:

Identify under-$1 stocks experiencing meaningful recent selling pressure that deserve fundamental investigation.