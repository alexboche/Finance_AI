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

### Unresolved Question

The learner has not yet answered:

> Should the airline take a long or short forward position in jet fuel to hedge its future purchase, and what happens to the hedge if jet fuel prices rise?

Do not record this concept as mastered until the learner answers and the reasoning has been discussed.

## Confirmed Mastery

No concepts have yet been assessed as mastered.

## Likely Next Steps

1. Discuss the airline hedge and establish the sign convention for long and short forward positions.
2. Write the physical exposure and derivative payoff separately, then combine them to show how the hedge stabilizes the effective purchase price.
3. Contrast forwards with options using the same airline example.
4. Introduce hedgers, speculators, and arbitrageurs from Hull Chapter 1.

## Repository State

- Standing course instructions were committed as `812bf1e` with subject `docs(course): establish derivatives learning charter`.
- Course work is currently on branch `docs/financial-derivatives-course-instructions`.
- Commit and push coherent learning milestones periodically.
