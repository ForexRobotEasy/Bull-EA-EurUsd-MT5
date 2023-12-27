# Bull EA EurUsd MT5

This is a sample Expert Advisor (EA) code for trading the EURUSD currency pair in MetaTrader 5 (MT5). The code is provided by Forex Robot Easy Team, and more information about the product can be found on their website [here](https://forexroboteasy.com/forex-robot-review/bull-ea-eurusd-mt5-review-low-risk-forex-software-with-high-backtest-results/).

## Functionality

The Bull EA EurUsd MT5 Expert Advisor is designed to execute buy and sell orders on the EURUSD currency pair based on price action and modern strategies. It uses a simple logic to determine whether to buy or sell:

1. On each tick event, the EA checks if there is an open position.
2. If there is no open position, it calculates the current price and the previous price.
3. If the current price is higher than the previous price, it executes a buy order at the market price with a stop loss (SL) and take profit (TP) level.
4. If the current price is lower than the previous price, it executes a sell order at the market price with a SL and TP level.
5. The SL and TP levels are defined by the variables `SL` (Stop Loss in pips) and `TP` (Take Profit in pips).

## Libraries and Functions

The code includes the `Trade` library, which provides necessary functions for trading operations. This library allows the EA to interact with the trading platform and execute orders.

## Initialization

The `OnInit()` function initializes the expert advisor. In this function, the symbol is set to 'EURUSD' using the `SymbolSet()` function.

## Tick Events

The `OnTick()` function is called on each tick event. It checks if there is an open position using the `PositionSelect()` function. If there is no open position, it calculates the current price and the previous price using the `SymbolInfoDouble()` function.

If the current price is higher than the previous price, it executes a buy order at the market price using the `OrderSend()` function. The order volume is set to 0.01, and the SL and TP levels are calculated based on the `SL` and `TP` variables.

If the current price is lower than the previous price, it executes a sell order at the market price using the `OrderSend()` function. Again, the order volume is set to 0.01, and the SL and TP levels are calculated based on the `SL` and `TP` variables.

## Deinitialization

The `OnDeinit()` function is called when the expert advisor is deinitialized. In this function, any open positions are closed using the `PositionClose()` function, if there are any open positions.

## Product Description

This sample code serves as an example of how the Bull EA EurUsd MT5 Expert Advisor can work. It is not the official developer's code, but it demonstrates the basic functionality of the product.

The Bull EA EurUsd MT5 is a low-risk forex software with high backtest results. It uses price action and modern strategies to execute buy and sell orders on the EURUSD currency pair. The EA aims to take advantage of market trends and generate profits.

Please note that this code is provided as a sample and may need to be modified or customized to suit individual trading strategies or preferences. For the official developer of this product and more information, it is recommended to visit the website [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/bull-ea-eurusd-mt5-review-low-risk-forex-software-with-high-backtest-results/) or use the MQL5 platform.
