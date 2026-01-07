# wids2025-26

I've added a small report on the things I learnt from the github links (mainly the first one)

Here is the stuff that I've done regarding the final submission that is assignment-final.
## Model Setup
The asset price follows the CEV stochastic differential equation

$ dS_t = r S_t \, dt + \sigma S_t^{\gamma} \, dW_t $

50,000 Monte Carlo paths with 252 time steps\
Random seed is 42

## Simulation Method
The CEV process is simulated using the Euler–Maruyama discretization. At each step, drift and diffusion terms are applied, and prices are floored at a small positive value to avoid numerical instability. Sample paths are visualized for γ = 0.5, 1.0, and 1.5 to observe how elasticity affects volatility behavior.

## Option Pricing
European call options with strike K = 100 are priced using Monte Carlo estimation. The discounted payoff is averaged across paths, and statistical diagnostics are reported, including standard error and a 95 percent confidence interval. As a consistency check, the γ = 1 case is compared directly with the analytical Black–Scholes price.

## Implied Volatility
Implied volatility is computed by inverting the Black–Scholes formula using root finding. For a fixed γ, call prices are generated across multiple strikes, and the corresponding implied volatilities are plotted to study skew or smile effects.

## Current issue....... there is no smile :(
