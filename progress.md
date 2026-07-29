# Financial Derivatives Course — Progress and Continuity Log

Last updated: 2026-07-28

## How to Resume

Read this file together with `FINANCIAL_DERIVATIVES_COURSE_INSTRUCTIONS.md` before continuing the course. Resume from the unresolved question in **Current Position** unless the learner asks to change direction.

Update this log after meaningful developments, including completed topics, demonstrated understanding, recurring confusion, changes in learning preferences, assigned exercises, and decisions about what to study next. Keep it concise enough to scan at the start of a new session.

## Course Goal

Develop a rigorous, practical understanding of financial derivatives, with broad coverage and particular emphasis on commodity trading and energy commodities.

## Learner Profile

- The learner has a PhD in economics.
- The learner has very little prior knowledge of finance.
- Assume strong economic intuition, probability, and mathematical maturity.
- Introduce finance-specific vocabulary, institutional mechanics, market conventions, and trading practice from first principles.
- Move quickly through familiar economics while being explicit about positions, cash flows, units, timing, and sign conventions.
- Distinguish no-arbitrage pricing from forecasting and equilibrium reasoning.

## Primary Sources

- John C. Hull, *Options, Futures, and Other Derivatives*, Eighth Global Edition (2012), located at `/Users/alex/programming/Finance_ai/Hull OPTIONS, FUTURES, AND OTHER DERIVATIVES.pdf`.
- Ilia Bouchouev, *Virtual Barrels* (2024), located at `/Users/alex/programming/Finance_ai/Bouchouev - Virtual Barrels 2024.pdf`.
- Hull is the main source for foundational theory. Bouchouev and other high-quality sources should provide commodity and energy-market context.

The two PDFs are local reference materials and are intentionally excluded from Git tracking.

## Current Position

### Lesson 1: What Problem Does a Derivative Solve?

Introduced:

- A derivative is a contract whose value depends on an underlying price, rate, index, or event.
- Energy underlyings can include crude oil, natural gas, refined products, electricity, and commodity price spreads.
- A forward or futures contract creates an obligation to transact later at an agreed price.
- A long forward agrees to buy; a short forward agrees to sell.
- An option gives its buyer a right without requiring exercise, in exchange for an upfront premium.
- The initial energy example is an airline that must buy 1 million gallons of jet fuel in three months and wants protection against rising fuel prices.

### Checkpoint Response

The learner correctly answered that the airline should take a **long forward position**: the airline's operating exposure loses value when jet fuel prices rise, while a long forward gains value when the underlying price rises.

For 1 million gallons with a forward price of $2.50 per gallon and a maturity market price of $3.00, the learner also correctly calculated:

- unhedged physical purchase cost: $3 million;
- long-forward payoff: +$500,000; and
- net hedged cost: $2.5 million.

This demonstrates the sign convention and the price-lock calculation:

`physical cost - forward payoff = Q × S_T - Q × (S_T - K) = Q × K`.

### Current Question

The course contrasted the symmetric price lock from a long forward with the asymmetric protection from a call option. The example uses 1 million gallons, a $2.50 strike, and a $0.10-per-gallon option premium.

The learner's responses subtracted the $100,000 premium from the effective cost. This revealed a sign issue: because the airline is buying the call, the premium is a cost and must be added to positive cost figures. The correct calculations are:

- At `S_T = $3.00`, physical cost is $3 million, option payoff is $500,000, premium is $100,000, and total effective cost is $2.6 million.
- At `S_T = $2.00`, physical cost is $2 million, option payoff is zero, premium is $100,000, and total effective cost is $2.1 million.

Clarified terminology:

- **Option payoff** excludes the premium: `max(S_T - K, 0)`.
- **Net option P&L** includes the premium: `max(S_T - K, 0) - c`, ignoring the premium's time value.
- For the two scenarios, the option payoffs are $500,000 and zero, while net option P&L is +$400,000 and -$100,000.

The call hedge's all-in unit cost is `min(S_T, K) + c`. With `K = $2.50` and `c = $0.10`, it is cheaper than the $2.50 forward hedge when `S_T < $2.40`, equal at $2.40, and more expensive above $2.40.

Introduced Hull's three participant roles:

- a **hedger** uses derivatives to reduce an exposure arising elsewhere;
- a **speculator** uses derivatives to create or increase exposure; and
- an **arbitrageur** combines positions to exploit inconsistent prices without net risk in the idealized model.

Emphasized that the participant's overall economic position—not the derivative in isolation—determines the classification.

For an oil producer expecting to sell 100,000 barrels in six months at a forward price of $75, the learner correctly identified a **short forward** and classified the producer as a **hedger**. At `S_T = $60`, the learner correctly gave the payoff as `(75 - 60) × 100,000 = $1.5 million`. Combined with $6 million of physical sales revenue, this locks total revenue at $7.5 million.

The next topic is the institutional distinction between OTC forwards and exchange-traded futures, followed by the basis risk that arises when an energy firm's physical exposure does not exactly match a listed contract.

## Confirmed Mastery

- A future commodity buyer hedges rising prices with a long forward position.
- A long forward's maturity payoff is `Q × (S_T - K)`.
- Combining the physical purchase with the long forward locks the effective purchase price at `K`, ignoring basis risk and other frictions.
- A future commodity seller hedges falling prices with a short forward position.
- A short forward's maturity payoff is `Q × (K - S_T)`.
- Hedger, speculator, and arbitrageur are classifications of the participant's overall position, not labels inherent to a particular contract.

Needs reinforcement:

- An option buyer pays the premium. When expressing outcomes as positive costs, add the premium; when expressing signed cash flows, the premium is negative.
- Keep **payoff** distinct from net **profit/P&L**.

## Likely Next Steps

1. Compare OTC forwards with exchange-traded futures.
2. Explain standardization, clearing, margin, daily settlement, liquidity, and counterparty risk.
3. Introduce basis risk and cross-hedging in energy markets.
4. Reinforce the premium's sign and the distinction between payoff and net P&L.

## Repository State

- Standing course instructions were committed as `812bf1e` with subject `docs(course): establish derivatives learning charter`.
- Course work is currently on branch `docs/financial-derivatives-course-instructions`.
- Commit and push coherent learning milestones periodically.
