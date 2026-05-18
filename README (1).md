# Barrier Option Pricing using Binomial Tree
## Project Overview
- This Project focuses on pricing an "Up-and-out Barrier Call Option" using the Binomial Tree Model.
- Barrier options are a class of exotic options whose value depends on whether the underlying asset price reaches a predefined level during the life of the option.
- In addition, a "Monte Carlo Simulation" is uded for comparison to better understand the pricing behavior of the model.

## Objective:
- To implement the Binomial Tree model for pricing a barrier option.
- To Study the impact of the barrier level on option value.
- To Compare results with Monte Carlo Simulation.
- To Understand the sensitivity of barrier options.

### Tools and Technologies:
- Python
- Numpy
- Jupyter Notebook

## Model details: 
### Primary Model
- Model used : Binomial Tree Model
- Option Type : Up-and-Out Barrier Call Option
- Method : Risk-neutral Valuation
### Comparison Model
- Model used : Monte Carlo Simulation
- Used to validate and compare pricing results

## Parameters Used
| Parameter | Description | Value |
| S0 | Initial S&P 500 value | 7408 |
| K | Strike Price | 7408 |
| B | Barrier Level | Variable |
| σ | Volatility | 0.1843 |
| r | Risk-free Rate | 0.0361 |
| q | Dividend Yield | 0.0106 |
| T | Time to Maturity | 1 Year |
| N | Time Steps (Binomial) |1000 |

## Key Feature:
- The Option is " Knocked out (becomes Zero) if the underlying asset price exceeds the barrier level at any point before maturity.
- If the barrier is not reached, the option behaves like a standard European Call Option.

## Results & Analysis: 
- The option price is highly sensitive to the barrier level.
- When the barrier is close to the current asset price, the option value becomes very low or zero due to a high probability of knock-out.
- As the barrier level increases, the option value increases.
- For sufficiently high barrier values, the option behaves similarly to a standard European call option.

At this stage, the results are based on the Binomial Tree model. Further analysis using Monte Carlo Simulation is planned to compare and validate the pricing results.


## Limitations:
- The Binomial Tree Model uses discrete time steps.
- Monte Carlo Simulation requires a large number of simulations for accuracy.
- Assumes constant volatility and interest rates.
- Barrier monitoring is done at discrete time intervals.

## Conclusion:
The project shows that barrier option pricing is strongly affected by the barrier level. Lower barriers result in lower option values due to a higher probability of knock-out, while higher barriers increase the option price. The Binomial Tree model effectively captures this behavior and provides a clear framework for pricing. Future work can include Monte Carlo simulation for comparison.

## Group Members:
1. Yu Chen
2. Laaya Fani
3. Mitu Mevada
