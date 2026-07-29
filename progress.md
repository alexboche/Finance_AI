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

The next step is to contrast the symmetric price lock from a long forward with the asymmetric protection from a call option. Use an airline example with a $2.50 strike and a $0.10-per-gallon option premium, examining maturity prices of $3.00 and $2.00 per gallon.

## Confirmed Mastery

- A future commodity buyer hedges rising prices with a long forward position.
- A long forward's maturity payoff is `Q × (S_T - K)`.
- Combining the physical purchase with the long forward locks the effective purchase price at `K`, ignoring basis risk and other frictions.

## Likely Next Steps

1. Contrast forwards with call options using the airline example.
2. Show how a call caps the effective fuel price while preserving the benefit of falling prices.
3. Discuss the option premium as the price of retaining that favorable-price exposure.
4. Introduce hedgers, speculators, and arbitrageurs from Hull Chapter 1.

## Repository State

- Standing course instructions were committed as `812bf1e` with subject `docs(course): establish derivatives learning charter`.
- Course work is currently on branch `docs/financial-derivatives-course-instructions`.
- Commit and push coherent learning milestones periodically.
