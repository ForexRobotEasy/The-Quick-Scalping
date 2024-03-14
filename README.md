# The Quick Scalping

The Quick Scalping is a custom indicator designed to filter out short-term price fluctuations and generate buy or sell signals based on the difference between the current price and a moving average. This code provides a basic implementation of the indicator and can be customized by adjusting the moving average period and sensitivity value.

## Input Parameters

- **MA_Period**: Moving Average period (default: 20)
- **Sensitivity**: Sensitivity value for buy or sell signals (default: 0.5)

## Indicator Initialization

The `OnInit` function is responsible for initializing the indicator. It creates a moving average using the specified period and assigns the handle to the global variable `MA_Handle`.

## Indicator Deinitialization

The `OnDeinit` function is called when the indicator is removed from the chart. It deletes the previously created moving average object using the `ObjectDelete` function.

## Indicator Calculation

The `OnCalculate` function is the main calculation function of the indicator. It is called for each new tick received. The function filters out short-term price fluctuations by calculating the moving average value using the `iMA` function. The difference between the current price and the moving average is then calculated.

- If the difference is greater than the sensitivity value, a buy signal is generated (place buy order code can be added here).
- If the difference is less than the negative sensitivity value, a sell signal is generated (place sell order code can be added here).

The moving average is also drawn on the chart using the `ObjectCreate` function to visualize the indicator's values.

## Product Description

The Quick Scalping is a fast forex trading indicator that aims to filter out short-term price fluctuations and generate buy or sell signals based on customizable moving average settings. It is designed to assist traders in identifying potential entry and exit points in the market. By utilizing the moving average and sensitivity parameters, the Quick Scalping provides a flexible tool for traders to adapt to different market conditions and trading strategies.

Please note that ForexRobotEasy is not the official developer of this product. We only provide this code as a sample implementation that can work as described in the official product. For detailed reviews and trading results of this product, please visit the official developer's website at [https://forexroboteasy.com/forex-robot-review/quick-scalping-review-fast-forex-trading-with-customizable-ma-settings/](https://forexroboteasy.com/forex-robot-review/quick-scalping-review-fast-forex-trading-with-customizable-ma-settings/). To find the official developer of this product, please refer to MQL5.
