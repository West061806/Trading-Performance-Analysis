# Trading Performance Analysis

## Overview
An analysis of the performance of a futures trader across multiple funded accounts using statistical metrics including win rate, expectancy, profit factor, Sharpe ratio, drawdown, and a custom Edge Score built to stress-test results against sample size uncertainty.

## Key Findings

Across all three accounts combined (152 trades), the blended performance showed a 36.8% win rate with a positive expectancy of 3.84 USD per trade. However, this masked significant differences between accounts. AQ01011 (30 trades, now closed) and the early live account history were both unprofitable, while AQ09244 (106 trades) was clearly profitable overall, ending with a net P/L of over +1,600 USD.

Looking at AQ09244 specifically over time, performance showed a sustained recovery beginning in mid-May — consistent with the period after NYSC camp. This recovery was accompanied by a reduction in drawdown severity, not just an increase in profit, suggesting risk management improved alongside results rather than profit coming from larger, riskier bets. Maximum drawdown on this account was -1,352.55 USD.

AQ09244's win rate of 43.4% combined with a win/loss ratio of 1.81 produced a profit factor of 1.25 and an annualised Sharpe ratio of 1.81 — both genuinely solid results for a discretionary futures strategy.

The live account, now at 16 trades and net +457.45 USD, shows an even stronger profit factor (1.36) and Sharpe ratio (1.96), though this is based on a much smaller sample.

To stress-test both results, an Edge Score was calculated — expectancy computed using the conservative (95% confidence interval lower-bound) win rate rather than the actual observed win rate. Both accounts produced a negative Edge Score (AQ09244: -0.06, Live: -0.81), meaning that while actual performance has been profitable, neither account yet has enough trades to statistically rule out the possibility that the true long-run win rate is low enough to erase the edge. This is not evidence against the strategy — it reflects the genuine uncertainty that comes with limited sample size, particularly for the 16-trade live account.

A direct comparison of trade outcome distributions before and after May 15 supports this. In the full trading history, large winning trades in the 400-600 USD range made up a small minority of total trades. Isolating only trades since May 15 shows that same range of large wins occurring proportionally more often relative to the smaller number of trades in that window — indicating that recent trading reflects a genuine shift in outcomes, not simply a few lucky trades diluted across a longer history. This is consistent with the trader's own assessment that skill and risk management improved meaningfully following NYSC camp, rather than the recovery being attributable to chance alone.

Overall: results to date are encouraging and the underlying risk management appears to have improved meaningfully since May. The strategy is not yet statistically proven, but the data does not contradict it either — more trades are needed before treating the edge as confirmed.


## Data Source
Personal trade history exported from Aquafutures trading platform across three accounts (AQ01011, AQ09244, VOL Live Account)

## Tools
- Python
- Pandas
- Matplotlib
- Numpy

## Files
- `Trading Performance.ipynb` — Main analysis notebook
- `trades_list_AQ01011.csv` 
- `trades_list_AQ09244.csv`
- `trades_list_VOL_Live_Account.csv`
