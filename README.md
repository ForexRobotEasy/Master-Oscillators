# Master Oscillators

Master Oscillators is a trading strategy that combines multiple oscillators, including RSI, CCI, and Stochastic, to identify potential trading opportunities in the Forex market. This code serves as a sample implementation of the strategy, and it is not the official product developed by Forex Robot Easy.

For detailed reviews and trading results of the official Master Oscillators product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/master-oscillators-review-streamline-your-forex-trading-strategy/).

## Input Parameters

- RSI_Period: The period used for calculating the RSI indicator.
- RSI_Overbought: The overbought level for the RSI indicator.
- RSI_Oversold: The oversold level for the RSI indicator.
- CCI_Period: The period used for calculating the CCI indicator.
- CCI_Overbought: The overbought level for the CCI indicator.
- CCI_Oversold: The oversold level for the CCI indicator.
- Stochastic_K_Period: The period used for calculating the %K line of the Stochastic indicator.
- Stochastic_D_Period: The period used for calculating the %D line of the Stochastic indicator.
- Stochastic_Slowing: The slowing period used for calculating the Stochastic indicator.
- Stochastic_Overbought: The overbought level for the Stochastic indicator.
- Stochastic_Oversold: The oversold level for the Stochastic indicator.
- MA_Period: The period used for calculating the moving average.
- MA_Method: The method used for calculating the moving average.

## Global Variables

- MA_Filter: A boolean variable indicating whether to use the moving average filter or not.
- Lot_Size: The lot size used for opening trades.
- Kelly_Criterion: A boolean variable indicating whether to use the Kelly Criterion for position sizing or not.
- Risk_Percentage: The risk percentage used for position sizing if the Kelly Criterion is not enabled.
- Stop_Loss: The stop loss level used for trades.
- Take_Profit: The take profit level used for trades.

## Custom Indicator Functions

- RSI(): Calculates the RSI value based on the input parameters.
- CCI(): Calculates the CCI value based on the input parameters.
- Stochastic(): Calculates the Stochastic value based on the input parameters.

## Trading Functions

- OpenTrade(): Performs the necessary actions to open a trade.
- CloseTrade(): Performs the necessary actions to close a trade.

## Calculation Functions

- CalculateLotSize(): Calculates the lot size based on user-defined criteria.
- CalculateStopLoss(): Calculates the stop loss level based on user-defined criteria.
- CalculateTakeProfit(): Calculates the take profit level based on user-defined criteria.

## Main Program

The main program is executed on each tick. It first checks if the MA filter is enabled. If enabled, it calculates the moving average and performs the trading logic based on the MA filter. If the bid price is above the moving average, it checks the RSI signal. If the RSI value is below the oversold level, it opens a trade. If the bid price is below the moving average, it checks the CCI signal. If the CCI value is above the overbought level, it opens a trade.

If the MA filter is not enabled, it checks the RSI signal directly. If the RSI value is below the oversold level, it opens a trade.

The program also includes a section for closing trades based on user-defined criteria.

## OnDeinit

The OnDeinit function is executed when the EA is removed from the chart or the terminal is closed. It performs necessary cleanup actions.

Please note that ForexRobotEasy is not the official developer of this product. This code serves as a sample implementation of the Master Oscillators strategy. To find the official developer of this product, please use MQL5.
