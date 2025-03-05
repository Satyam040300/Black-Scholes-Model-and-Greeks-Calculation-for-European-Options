# Black-Scholes Model and Greeks Calculation for European Options

This project implements the **Black-Scholes Model** for pricing European **call** and **put options** and calculates the **Greeks** (Delta, Gamma, Vega) using finite difference methods. The Greeks help assess the sensitivity of the option price to changes in key parameters such as stock price, volatility, and time to maturity. 

By extending the Black-Scholes model with the calculation of these sensitivities, this project provides deeper insights into risk management and option pricing in financial markets.

## Project Overview

The Black-Scholes model is widely used for pricing options based on the following variables:
- **S₀**: Initial stock price
- **K**: Strike price
- **T**: Time to maturity (in years)
- **r**: Risk-free interest rate
- **σ**: Volatility (standard deviation of stock returns)

This project extends the model by calculating the **Greeks**:
- **Delta**: Sensitivity of the option price to changes in the stock price
- **Gamma**: Sensitivity of Delta to changes in the stock price
- **Vega**: Sensitivity of the option price to changes in volatility

## Files

- `Satyam_Black_Scholes_Greeks_Calculation_(Delta,_Gamma,_Vega).ipynb`: Contains the implementation of the Black-Scholes model for **call** and **put** options, along with functions to calculate **Delta**, **Gamma**, and **Vega** using finite difference methods.
- `requirements.txt`: Lists the required Python libraries (`scipy`, `math`).

## Usage

You can calculate the **call** and **put** option prices and their Greeks by calling the functions in the `black_scholes.py` file with the following parameters:


S0 = 100    # Initial stock price

K = 100     # Strike price

T = 1       # Time to maturity (in years)

r = 0.05    # Risk-free interest rate

sigma = 0.2 # Volatility (20%)

# Calculate the Call and Put prices

call_price = black_scholes_call(S0, K, T, r, sigma)

put_price = black_scholes_put(S0, K, T, r, sigma)

# Calculate Greeks

delta = calculate_delta(S0, K, T, r, sigma)

gamma = calculate_gamma(S0, K, T, r, sigma)

vega = calculate_vega(S0, K, T, r, sigma)

# Output the results
print(f"Call Option Price: {call_price}")

print(f"Put Option Price: {put_price}")

print(f"Delta: {delta}")

print(f"Gamma: {gamma}")

print(f"Vega: {vega}")

# Project Insights
The Black-Scholes model provides a theoretical estimate for the price of European options based on stock price, volatility, and time to maturity.
The Greeks help in assessing how sensitive the option price is to changes in the underlying parameters, providing valuable insights for risk management and option strategy optimization.
The model assumes European options, which can only be exercised at expiration.

# Skills Learned

Option Pricing using the Black-Scholes model

Greeks Calculation (Delta, Gamma, Vega) for option sensitivity analysis

Quantitative Finance and Mathematical Finance principles

Python Programming for implementing financial models

Finite Difference Methods for numerical differentiation

# Future Work
This project can be extended by:

Implementing additional Greeks such as Theta and Rho to complete the set of primary sensitivities.
Incorporating Monte Carlo simulations to explore alternative option pricing methods.
Building a more interactive tool for real-time option pricing based on live stock data.

