# Zeus — Public Audit Trail

US/EU large-cap quality rotation strategy · **forward paper test from 2026-04-16** · review **2026-10-16** (6 months min).

**0 client capital deployed.** All snapshots below are forward paper test on real-time market data with frozen parameters. No broker capital is at risk.

## What this proves

- **SHA-256 integrity hashes** verify the strategy engine files have not changed since genesis.
- **Drift reports** show forward-paper performance vs backtest expected range, calibrated by Harvey-Liu 2015 non-linear haircut.
- **Daily snapshots** are append-only commits — every line in the table below is a separate cron run.

## What this never publishes

- Strategy parameters (slot count, hold weeks, pacing, RSI thresholds, EMA lengths, sector caps)
- BUY/SELL signal names or types
- Scoring formula thresholds (V11.2 score gates, conviction flags)
- Frozen universe list (the 68 stocks)
- Anything that would let someone replicate the strategy from this repo

## Reference claims (source: claims_sheet.md authoritative)

- Backtest 19y CORE 2007-2026 : CAGR **+27.47%** · Sharpe **1.51** · Calmar 1.24 · MaxDD -22.21% · 495 trades
- Backtest 11y MODERN 2015-2026 : CAGR +24.85% · Sharpe 1.41 (proxy for live regime)
- Backtest 31y FULL 1995-2026 : CAGR +20.99% · Sharpe 1.20 (long-term stress, includes survivorship bias caveat pre-2005)
- Live expected (Harvey-Liu 2015 haircut, discount 0.90) : CAGR **22-23%** · Sharpe 1.30-1.40
- α FF5+MOM : +19.08%, t=+5.23, p<0.0001 (Newey-West HAC)
- DSR Bailey-de Prado 2014 : 0.9998
- Walk-forward 24 folds : 17/24 GREEN
- MC 1000 seeds : Sharpe IC95 [1.12, 1.91]

## Review rule

`review = max(2026-10-16, n_trades_closed_live ≥ 10)` — first GO/NO-GO capital deployment decision requires 6 months calendar AND ≥10 closed trades (statistical power requirement, DSR Bailey-de Prado).

## Disclaimer

Educational analytics tool. **Not investment advice.** Past performance does not guarantee future results. Forward paper test means no client capital is deployed; the strategy tracks real market data with frozen parameters for transparency and academic rigor. Live execution introduces additional friction (slippage, taxes, behavioral factors) not fully captured in backtest. Consult a licensed financial advisor before any investment decision.

---

## Snapshots index

| Date | Git SHA | Files hashed | Drift file | Portfolio state |
|------|---------|-------------|------------|----------------|
| 2026-04-18 | `4299e4ca` | 4/4 frozen | [drift](2026-04-18_drift_report.json) | [state](2026-04-18_portfolio_state.json) |
| 2026-04-20 | `08eb86b4` | 4/4 frozen | [drift](2026-04-20_drift_report.json) | [state](2026-04-20_portfolio_state.json) |
| 2026-04-21 | `9eba0319` | 4/4 frozen | [drift](2026-04-21_drift_report.json) | [state](2026-04-21_portfolio_state.json) |
| 2026-04-22 | `2cf2c42f` | 4/4 frozen | [drift](2026-04-22_drift_report.json) | [state](2026-04-22_portfolio_state.json) |
| 2026-04-24 | `909f22de` | 4/4 frozen | [drift](2026-04-24_drift_report.json) | [state](2026-04-24_portfolio_state.json) |
| 2026-04-26 | `393af8b3` | 4/4 frozen | [drift](2026-04-26_drift_report.json) | [state](2026-04-26_portfolio_state.json) |
| 2026-04-27 | `eddd9638` | 4/4 frozen | [drift](2026-04-27_drift_report.json) | [state](2026-04-27_portfolio_state.json) |
| 2026-04-28 | `ab91fa24` | 4/4 frozen | [drift](2026-04-28_drift_report.json) | [state](2026-04-28_portfolio_state.json) |
| 2026-04-30 | `2ce27ea9` | 4/4 frozen | [drift](2026-04-30_drift_report.json) | [state](2026-04-30_portfolio_state.json) |
| 2026-05-02 | `06793a63` | 4/4 frozen | [drift](2026-05-02_drift_report.json) | [state](2026-05-02_portfolio_state.json) |
| 2026-05-03 | `e5a10c70` | 4/4 frozen | [drift](2026-05-03_drift_report.json) | [state](2026-05-03_portfolio_state.json) |
