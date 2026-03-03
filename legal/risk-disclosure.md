---
title: Risk Disclosure Statement
description: Comprehensive risk disclosure for pairs trading and securities trading
---

# Risk Disclosure Statement

**Effective Date:** March 4, 2026  
**Last Updated:** March 4, 2026

---

## ⚠️ MANDATORY READING

**This Risk Disclosure Statement outlines the significant risks associated with securities trading, pairs trading strategies, and use of PairSync's educational platform.**

**By using PairSync and engaging in any trading activity based on information learned from the platform, you acknowledge that you have read, understood, and accepted these risks.**

---

## Executive Summary of Risks

**TRADING SECURITIES INVOLVES SUBSTANTIAL RISK OF LOSS.**

**Key Risks:**
- 📉 **Market Risk:** You can lose all or more than your invested capital
- 📊 **Model Risk:** Statistical patterns can fail without warning
- ⚡ **Execution Risk:** Real trading costs significantly reduce theoretical returns
- 💸 **Liquidity Risk:** You may be unable to exit positions at desired prices
- 📈 **Leverage Risk:** Margin amplifies both gains AND losses
- 🔻 **Short Selling Risk:** Losses can be unlimited on short positions
- 🌍 **Systemic Risk:** Market-wide events can overwhelm any strategy

**ONLY TRADE WITH CAPITAL YOU CAN AFFORD TO LOSE ENTIRELY.**

---

## 1. General Market Risk

### 1.1 Risk of Loss
**YOU CAN LOSE MONEY trading securities, including pairs trading strategies.**

Losses can result from:
- Adverse price movements
- Changes in market conditions
- Breakdown of historical relationships
- Unexpected events (earnings surprises, geopolitical shocks)
- General market declines

**There is NO guarantee you will make money. You may lose your entire investment.**

### 1.2 Volatility Risk
Securities prices fluctuate, sometimes dramatically:
- **Intraday volatility:** Prices can swing 5-10% or more in a single day
- **Overnight gaps:** Prices can open significantly different from the prior close
- **Flash crashes:** Sudden, extreme price drops (e.g., May 2010 Flash Crash)
- **Volatility clustering:** High volatility periods tend to persist

**Pairs trading does NOT eliminate volatility risk, though it may reduce it relative to directional strategies.**

### 1.3 Systematic Risk
Some risks cannot be diversified away:
- **Market crashes:** 2008 financial crisis, 2020 COVID crash
- **Interest rate changes:** Fed policy shifts
- **Regulatory changes:** New trading rules or restrictions
- **Economic recessions:** Broad economic downturns

**Even "market-neutral" strategies can lose money during systemic events.**

---

## 2. Pairs Trading Specific Risks

### 2.1 Cointegration Breakdown
**The central assumption of pairs trading - that two assets maintain a stable relationship - CAN FAIL.**

**Causes of cointegration breakdown:**
- **Business divergence:** Companies change business models, enter new markets
- **Mergers and acquisitions:** One company is acquired, permanently altering relationship
- **Sector rotation:** Industry dynamics shift (e.g., tech vs value)
- **Competitive changes:** New entrants, disruption, market share shifts
- **Financial distress:** One company faces bankruptcy risk
- **Regulatory changes:** Different regulatory treatment of the two assets

**Example:**  
Company A and Company B were historically cointegrated (both auto manufacturers). Company A pivots to electric vehicles and autonomous driving, while Company B focuses on traditional cars. The historical relationship breaks down permanently.

**Risk Impact:** You could wait indefinitely for mean reversion that never occurs, tying up capital and accumulating costs.

### 2.2 Correlation Risk
**Even cointegrated pairs can temporarily move in the same direction, causing losses on both legs.**

**When correlation spikes:**
- **Market crashes:** 2008, 2020 - most stocks fell together
- **Sector crises:** All banks fell in 2008, all tech stocks fell in 2022
- **Liquidity crunches:** Forced selling affects all stocks
- **Risk-off events:** Geopolitical shocks cause flight to safety

**Risk Impact:** You lose money on both the long AND short position simultaneously.

**Example:**  
You're long Stock A and short Stock B (both airlines). COVID-19 hits. Both stocks crash -60%. Your "market-neutral" position loses ~0% based on dollar neutrality, but if position sizing was off or leverage was used, you could face significant losses or margin calls.

### 2.3 Mean Reversion Timing Risk
**Mean reversion may take MUCH longer than expected.**

**Historical examples:**
- Pairs diverging for 6+ months before reverting
- Extended periods "this time is different"
- Opportunity cost of capital being tied up

**Risk Impact:**
- Your capital is locked in non-performing trades
- Margin interest accumulates (if leveraged)
- Psychological stress and potential for premature exit at a loss

### 2.4 Divergence Before Convergence
**Pairs can diverge further BEFORE they converge.**

**The "can stay irrational longer than you can stay solvent" problem:**
- You enter a trade at Z-score +2.0 (expecting reversion)
- The spread widens to Z-score +3.5 before reverting
- You face margin calls or stop-loss triggers
- You're forced out at max loss before the eventual reversion

**Risk Impact:** Technical "correctness" doesn't prevent interim losses.

### 2.5 Half-Life Instability
**The speed of mean reversion (half-life) is not constant.**

- Historical average half-life: 15 days
- Current half-life: Could be 5 days OR 50 days
- Regime changes alter mean reversion speed

**Risk Impact:** Trades take longer to play out, increasing cost and reducing returns.

---

## 3. Execution Risks

### 3.1 Slippage
**Slippage is the difference between expected and actual execution price.**

**Causes:**
- Fast-moving markets
- Low liquidity (wide bid-ask spreads)
- Large order size relative to available liquidity
- High volatility periods

**Real-world impact:**
- Backtests assume execution at closing price (e.g., $50.00)
- Real execution: You buy at $50.08, sell at $49.92
- Per-trade slippage: 0.08-0.16%, or 8-16 basis points
- Over 100 trades/year: 8-16% drag on returns

**This can turn a profitable backtest into a losing live strategy.**

### 3.2 Transaction Costs
**Every trade incurs costs:**

#### Brokerage Commissions
- Traditional brokers: $1-$5 per trade ($2-$10 per round-trip pair)
- "Commission-free" brokers: Hidden costs in order routing

#### Regulatory Fees
- SEC fees: ~$5.10 per $1,000,000 of sales
- FINRA Trading Activity Fee: $0.000145 per share sold
- Exchange fees

#### Bid-Ask Spread
- Cost of crossing the spread (immediacy premium)
- Liquid stocks: 0.01-0.05% per trade
- Illiquid stocks: 0.10-1.00% per trade

**Total cost estimate:**
- Round-trip pair trade: 0.10-0.50% total cost
- 50 trades/year: 5-25% annual drag on returns

### 3.3 Market Impact
**Your orders move prices against you.**

**Larger positions:**
- Buying pressure pushes prices up (you pay more)
- Selling pressure pushes prices down (you receive less)
- More pronounced in illiquid markets

**Risk Impact:**  
Backtests assume NO market impact. Real trading for meaningful size degrades performance.

### 3.4 Timing Delays
**Real-world trading has delays:**
- Signal generation → decision → order placement: Minutes to hours
- Orders may execute at prices worse than when signal was generated
- Gap between closing legs (one fills, other doesn't immediately)

**Risk Impact:** "Leg risk" - partially filled pairs where only one side executes, leaving you exposed.

---

## 4. Short Selling Risks

### 4.1 Unlimited Loss Potential
**SHORT SELLING HAS THEORETICALLY UNLIMITED RISK.**

- **Long position:** Maximum loss = 100% (stock goes to $0)
- **Short position:** Maximum loss = UNLIMITED (stock can rise 200%, 500%, 1000%+)

**Example:**
- Short 100 shares at $50 = $5,000 position
- Stock rises to $150 = Loss of $10,000 (200% loss on original capital)
- Stock rises to $500 = Loss of $45,000 (900% loss)

**"Short squeezes" can cause explosive upward price movements.**

### 4.2 Hard-to-Borrow Costs
**Shorting requires borrowing shares, which has costs:**

- **Easy-to-borrow stocks:** 0.10-1.00% annual
- **Hard-to-borrow stocks:** 5-50% annual or MORE
- **Extreme cases:** 100%+ annual (essentially unshortable)

**These costs:**
- Are deducted daily from your account
- Are NOT included in PairSync backtests
- Can turn profitable backtests into losers

**Example:**
- Backtest shows 15% annual return
- Average hard-to-borrow cost: 8% annual
- Real return: 7% (before other costs)

### 4.3 Stock Recall Risk
**Your broker can FORCE you to close short positions:**

- Lender recalls shares (needs them back)
- Stock becomes hard-to-borrow
- Broker risk management decision
- **No advance warning required**

**Risk Impact:** Forced exit at an unfavorable price, potentially locking in losses.

### 4.4 Dividends and Corporate Actions
**When you short a stock, YOU pay dividends to the lender:**

- Stock pays $1 dividend → You pay $1 per share shorted
- Ex-dividend gap risk (stock drops less than dividend amount)

**Special dividends or spin-offs can create unexpected liabilities.**

### 4.5 Regulatory Restrictions
**Short selling can be restricted:**
- **Uptick rule:** Can only short on an uptick (rarely enforced now)
- **Short sale bans:** Regulators can ban shorting during crises (2008 financial crisis)
- **Disclosure requirements:** Large short positions may need reporting

---

## 5. Leverage and Margin Risks

### 5.1 Leverage Amplifies Losses
**Pairs trading is often done with leverage (margin):**

- **2x leverage:** A 5% loss = 10% loss to your capital
- **3x leverage:** A 5% loss = 15% loss to your capital
- **4x leverage:** A 5% loss = 20% loss to your capital

**Gains are amplified, but SO ARE LOSSES.**

### 5.2 Margin Calls
**If losses exceed available margin, your broker will issue a margin call:**

- You must deposit additional funds within 24-48 hours
- If you don't, broker LIQUIDATES your positions
- Liquidation happens at WORST possible time (during losses)
- You have no control over which positions are closed or at what prices

**Liquidation can turn temporary paper losses into permanent realized losses.**

### 5.3 Margin Interest Costs
**Borrowing on margin costs money:**
- Typical rates: 5-12% annual (varies by broker and market conditions)
- Interest accrues daily
- Compounds losses during drawdown periods

**Example:**
- $50,000 position on $25,000 capital (2x leverage)
- Margin interest: 8% annual
- $25,000 borrowed × 8% = $2,000/year in interest
- Must earn 8% just to break even on borrowed portion

### 5.4 Maintenance Requirements
**Minimum margin requirements can change:**
- Normal requirement: 25-30% minimum equity
- Volatile stocks: 40-100% requirement
- Broker discretion: Can raise requirements anytime

**Risk Impact:** Forced deleveraging or position closure during market stress.

---

## 6. Liquidity Risks

### 6.1 Illiquid Markets
**Not all stocks/pairs are equally liquid:**

**Liquid (major stocks):**
- Tight bid-ask spreads (0.01-0.02%)
- Deep order books
- Can trade size with minimal impact

**Illiquid (small-cap, foreign stocks):**
- Wide spreads (0.5-2%)
- Thin order books
- Significant market impact

**Risk Impact:** Illiquid pairs have higher costs and exit difficulty.

### 6.2 Inability to Exit
**You may be unable to close positions when needed:**
- Trading halts (circuit breakers, news pending)
- After-hours gaps (no liquidity outside market hours)
- Market crashes (everyone trying to exit simultaneously)

### 6.3 Flash Crashes and Extreme Events
**Sudden liquidity evaporation:**
- May 2010: Dow dropped 1,000 points in minutes
- October 1987: Black Monday (-22% in one day)
- March 2020: Circuit breakers triggered multiple times

**"Market-neutral" strategies are NOT immune to these events.**

---

## 7. Model and Statistical Risks

### 7.1 Model Overfitting
**CRITICAL RISK: PairSync's backtests are in-sample optimized.**

**What this means:**
- PairNet MLOps process was trained on the same data used for backtesting
- Entry/exit distances, timing, and parametizations were tuned to maximize historical performance
- This creates **overfitting** - the model learned noise, not true signal

**Out-of-sample performance expectation:**
- In-sample backtest: 15% annual return
- Out-of-sample reality: 9-12% (if you're lucky)
- Potential: 0% or negative

**This is THE #1 reason quantitative strategies fail when deployed live.**

### 7.2 Parameter Instability
**Optimal parameters change over time:**
- Z-score thresholds that worked 2015-2020 may not work 2025-2030
- Market regime changes
- Competition (more traders using similar strategies reduces edge)

### 7.3 Data Mining Bias
**With thousands of possible pairs, some will show good backtests purely by chance:**
- Test 10,000 pairs → 500 will show "statistical significance" at 95% level by luck alone
- Cherry-picking the best backtests doesn't mean they'll continue

### 7.4 Stationarity Assumption
**Pairs trading assumes spread stationarity (mean reversion).**

**But:**
- Markets are non-stationary (statistics change over time)
- What was stationary 2020-2023 may not be 2024-2027
- No guarantee stationarity persists

### 7.5 Black Swan Events
**Models assume normal distributions.**

**Reality:**
- Fat tails (extreme events more common than models predict)
- October 1987: 22% drop = ~20-sigma event (should never happen)
- 2008 crisis: Multi-sigma moves for weeks

**Your maximum expected loss is probably UNDERESTIMATED.**

---

## 8. Technology and Operational Risks

### 8.1 App Outages
**PairSync may be unavailable:**
- Server downtime
- Cyber attacks (DDoS)
- Maintenance windows
- Software bugs causing crashes

**Risk Impact:** Unable to access signals or data when needed for trading decisions.

### 8.2 Data Errors
**Market data can be incorrect:**
- Provider errors
- Stale prices
- Calculation bugs
- Display glitches

**Always verify data with multiple sources before trading.**

### 8.3 Cybersecurity
**Risks from cyber threats:**
- Account hijacking
- Data breaches
- Malware on your device
- Phishing attacks

**Use strong passwords, enable 2FA, and keep devices secure.**

### 8.4 Order Entry Errors
**Manual trading introduces human error:**
- Wrong symbol
- Wrong quantity (1000 shares vs 100)
- Wrong side (buy vs sell)
- Fat-finger mistakes ($5 vs $50 price)

**ALWAYS double-check orders before submission.**

---

## 9. Regulatory and Legal Risks

### 9.1 Pattern Day Trader Rule
**US regulation (FINRA Rule 4210):**
- 4+ day trades in 5 business days = Pattern Day Trader
- Requirement: $25,000 minimum account equity
- Violation: Trading frozen until compliance

**Impact on pairs trading:**
- Frequent entry/exit = many day trades
- Must maintain $25k minimum OR limit day trades

### 9.2 Wash Sale Rule
**IRC Section 1091:**
- Selling a security at a loss and repurchasing "substantially identical" security within 30 days
- Loss disallowed for current tax year
- Basis adjustment complicates tax reporting

**Pairs trading with frequent exits/re-entries can trigger wash sales.**

### 9.3 Securities Fraud
**Regulatory risks:**
- Insider trading (trading on non-public information)
- Market manipulation (pump and dump schemes)
- Front-running (trading ahead of known orders)

**Always comply with securities laws. Violations carry criminal penalties.**

### 9.4 International Regulations
**For non-US users:**
- Different short-selling rules (some countries ban it)
- Different margin requirements
- Different tax treatment
- Possible restrictions on accessing US markets

---

## 10. Psychological and Behavioral Risks

### 10.1 Emotional Decision-Making
**Common behavioral pitfalls:**
- **Revenge trading:** Trying to "get even" after losses
- **Overtrading:** Excessive activity driven by anxiety
- **FOMO:** Entering late due to fear of missing out
- **Anchoring:** Holding losers hoping to break even

**Pairs trading requires discipline to follow rules during stress.**

### 10.2 Overconfidence
**After early success:**
- Overestimating skill vs luck
- Taking excess risk
- Ignoring stop-losses
- Deviating from strategy

**Successful backtests can breed false confidence.**

### 10.3 Recency Bias
**Recent events disproportionately influence decisions:**
- Recent wins → take more risk
- Recent losses → become too conservative
- Past week's performance ≠ long-term expectation

### 10.4 Stress and Health
**Active trading is stressful:**
- Anxiety during drawdowns
- Sleep disruption
- Impact on work and relationships

**Only trade if you can handle the psychological burden.**

---

## 11. Specific Asset Class Risks

### 11.1 Equity (Stock) Pairs
- **Earnings risk:** Quarterly reports cause volatility
- **Analyst ratings:** Upgrades/downgrades create gaps
- **Sector correlation:** Industry-wide moves affect both legs
- **Delisting risk:** Stocks can be delisted or suspended

### 11.2 Cryptocurrency Pairs
**CRYPTOCURRENCY IS EXTREMELY VOLATILE AND RISKY:**
- **Extreme volatility:** 20-50% daily moves are common
- **24/7 trading:** No market close (overnight gaps)
- **Exchange risk:** Hacks, insolvency, fraud (FTX collapse)
- **Regulatory uncertainty:** Possible bans or restrictions
- **Manipulation:** Whale manipulation, wash trading
- **Custody risk:** "Not your keys, not your coins"
- **Technological risk:** Hard forks, network issues

**Crypto pairs trading is SIGNIFICANTLY riskier than stock pairs.**

### 11.3 International Stocks
- **Currency risk:** FX fluctuations impact returns
- **Political risk:** Government instability, nationalization
- **Liquidity risk:** Foreign markets may be less liquid
- **Regulatory differences:** Different reporting, rules

---

## 12. Costs and Fees Summary

**All-in costs can equal 5-20% of gross returns:**

| Cost Category | Typical Range | Impact |
|---------------|---------------|--------|
| Commissions | $0-$5/trade | 0-2% annually |
| Bid-Ask Spread | 0.01-0.50% | 2-10% annually |
| Slippage | 0.05-0.20% | 2-5% annually |
| Short borrowing | 0.10-10% | 0-10% annually |
| Margin interest | 5-12% on borrowed amount | 0-6% annually |
| Market impact | 0.01-0.10% | 1-5% annually |
| **Total Drag** | | **5-20%+ annually** |

**A 15% gross return backtest might yield 8-10% after costs (or less).**

---

## 13. Disclaimers Specific to PairSync

### 13.1 Educational Platform Only
**PairSync is NOT:**
- A trading system (no live execution)
- Investment advice (you decide what to trade)
- A guarantee of profitability

**PairSync backtests are educational examples, not predictions.**

### 13.2 Hypothetical Performance
**ALL backtests shown in PairSync:**
- ✓ Are based on historical data
- ✓ Assume perfect execution
- ✓ Exclude most real-world costs
- ✓ Used in-sample optimization
- ✗ Do NOT represent actual trading results
- ✗ Do NOT predict future performance

### 13.3 No Warranty
**PairSync makes NO guarantee about:**
- Accuracy of data or signals
- Profitability of any pair
- Continuation of historical patterns
- App availability or functionality

### 13.4 User Responsibility
**YOU are 100% responsible for:**
- Deciding whether to trade
- Position sizing and risk management
- Verifying data accuracy
- Executing trades properly
- Managing your own brokerage account
- Complying with all laws and regulations

---

## 14. Risk Management Best Practices

**While PairSync cannot provide personalized advice, general risk management principles include:**

### 14.1 Position Sizing
- Never risk more than 1-2% of capital on any single trade
- Avoid concentration (don't put all capital in one pair)
- Size positions based on volatility (smaller size for volatile pairs)

### 14.2 Stop-Losses
- Set maximum loss tolerance (e.g., exit if loss exceeds 5-10%)
- Don't "hope" for mean reversion indefinitely
- Accept losses and move on

### 14.3 Diversification
- Trade multiple pairs across sectors
- Mix asset classes (stocks, crypto if appropriate)
- Don't over-concentrate in correlated pairs

### 14.4 Leverage Limits
- Start with NO leverage (1x)
- Only use leverage if experienced and can handle losses
- Keep leverage conservative (2x max for most traders)

### 14.5 Paper Trading First
- Practice with simulated money before risking real capital
- Track results for 6-12 months
- Verify you can execute the strategy profitably

### 14.6 Continuous Monitoring
- Monitor positions daily (pairs trading isn't "set and forget")
- Watch for cointegration breakdown
- Be ready to exit losing positions

**These are NOT recommendations, but general educational principles. Consult a financial advisor for personalized guidance.**

---

## 15. Acknowledgment and Acceptance

**By using PairSync and engaging in any trading activity, you:**

✅ **Acknowledge** you have read and understood this entire Risk Disclosure Statement  
✅ **Understand** trading involves substantial risk of loss  
✅ **Accept** you could lose all or more than your invested capital  
✅ **Agree** PairSync is educational only and not investment advice  
✅ **Recognize** backtests are hypothetical and not predictive  
✅ **Assume** full responsibility for your own trading decisions  
✅ **Agree** to not hold PairSync liable for any trading losses  
✅ **Confirm** you will consult licensed professionals before trading  

**If you DO NOT accept these risks, DO NOT USE PAIRSYNC FOR TRADING.**

---

## 16. Questions or Concerns

**If you have questions about any risk:**

**Email:** mark@pair-sync.com  
**Subject:** "Risk Disclosure Question"

**We can provide general educational clarification, but cannot provide personalized risk assessments or recommendations.**

**For personalized guidance, consult:**
- A licensed financial advisor (for investment strategy)
- A risk management professional
- Your brokerage's risk desk

---

## 17. Required Statements

**CFTC Rule 4.41 (for trading futures, if applicable in future):**  
PAST PERFORMANCE IS NOT NECESSARILY INDICATIVE OF FUTURE RESULTS.

**SEC Regulation BI (Best Interest, if applicable):**  
PairSync is not a broker-dealer and does not provide recommendations subject to Reg BI.

**FINRA Notice:**  
PairSync is not a member of FINRA and does not provide brokerage services.

---

## Related Documents

- [Terms of Service](terms-of-service.md) - Your legal agreement with PairSync
- [Privacy Policy](privacy-policy.md) - How we handle your data
- [General Disclaimers](disclaimers.md) - Additional legal disclaimers
- [Compliance Notice](compliance-notice.md) - Regulatory compliance information

---

**Contact:** mark@pair-sync.com  
**Phone:** +61 408 881 692

*© 2026 PairSync. All rights reserved.*

**Last Updated:** March 4, 2026

---

## FINAL WARNING

**TRADING IS RISKY. LOSSES ARE REAL. PROCEED WITH CAUTION.**

**Never trade with money you need for:**
- Rent or mortgage
- Food and basic necessities
- Emergency funds
- Retirement savings
- Your children's education

**Only trade with "venture capital" you can afford to lose 100% of without impacting your life.**

**If in doubt, DON'T TRADE. Education and paper trading are risk-free alternatives.**
