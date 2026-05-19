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
- The underlying asset price is simulated using Geometric Brownian Motion (GBM).
- The barrier condition is applied by checking whether the asset price exceeds the barrier level at any point along each simulated path.
- The Monte Carlo approach is used to validate and compare the pricing results obtained from the binomial model.

## Parameters Used
| Parameter | Description | Value |
|----------|------------|------|
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
- Both discrete-time (binomial) and continuous-path (Monte Carlo) approaches are used for pricing and comparison.

## Results & Analysis: 
- The option price is highly sensitive to the barrier level.
- When the barrier is close to the current asset price, the option value becomes very low or zero due to a high probability of knock-out.
- As the barrier level increases, the option value increases.
- For sufficiently high barrier values, the option behaves similarly to a standard European call option.

- The Monte Carlo simulation produces results that are consistent with the binomial tree model, providing validation for the pricing approach.
Small differences between the two methods may arise due to:
   - Discrete time steps in the binomial model
   - Simulation error in Monte Carlo methods
- The analysis also shows that:
   - Increasing the number of time steps in the binomial tree improves accuracy (convergence).
   - Barrier options are more sensitive to volatility compared to standard options, as higher volatility increases the probability of hitting the barrier.



## Limitations:
- The Binomial Tree Model uses discrete time steps, which may introduce approximation errors for continuously monitored barriers.
- Monte Carlo Simulation requires a large number of simulated paths for higher accuracy.
- The model assumes constant volatility and interest rates.
- Barrier monitoring in the binomial model is discrete rather than continuous, which may lead to slight pricing differences.

## Conclusion:
The project shows that barrier option pricing is strongly affected by the barrier level. Lower barriers result in lower option values due to a higher probability of knock-out, while higher barriers increase the option price. 

Both the Binomial Tree model and Monte Carlo simulation provide consistent pricing results, confirming the validity of the approach. The comparison highlights the strengths and limitations of each method and provides a deeper understanding of barrier option behavior.

## Group Members:
1. Yu Chen
2. Laaya Fani
3. Mitu Mevada

