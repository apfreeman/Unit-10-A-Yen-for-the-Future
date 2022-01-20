# Unit 10 - Yen for the Future

## Summary of Models and Findings

![Yen Photo](Images/unit-10-readme-photo.png)

## Background

The financial departments of large companies often have to make foreign currency transactions when doing international business, while hedge funds are also interested in anything that will provide an edge in predicting currency movements. Hence, both are always eager to gain a better understanding of the future direction and risk of various currencies. 

In this assignment, I have tested the many time series tools I have learned in order to predict future movements in the value of the Canadian dollar versus the Japanese yen.

Below is the summary of my findings.


# Summary 

## Time-Series Forecasting

**Question:** Do you see any patterns, long-term and/or short? 

**Answer:** 
- **Short Term Patterns** There is a definite short term pattern showing a decline of the value of the CAD vs the JPY for the period 1991 to mid 1995. It can be seen from the plot that 1 Canadian dollar was buying around 138 Japanese yen. Over the next five and a half years this fell dramatically to the point that 1 Canadian dollar was buying around 60 Japanese Yen. Another short term pattern identified is a short term peak in the strength of the CAD vs the JPY around the start of 2018. Otherwise it can be noticed that in the short term there is a lot of volatility which is pretty typical for common currency pairs. 

- **Long Term Patterns** Observing the overall pattern for the CAD/JPY over the long term it can be seen that there is a general downward trend from 1990 to 2020. Excluding the significant downward trend from 1990 to 1996 and the peak in 2008 the trend is generally pretty flat over the long term. For example the value of the CAD vs the JPY in 2004 is very similar to the value in 2020.

**Question:** Do you see any patterns, long-term and/or short?

**Answer:** 
- **Short Term Patterns** Using the trend we can remove a lot of the short term volatility which helps us look at the overall trends. It can be seen that there is generally an upward trend that follows a downward trend. The duration of these trends are generally over a six month duration. Excluding 2020 it is observed that there is a shorter term trend in that the value of the CAD is stronger against the JPY at the start of each year compared to the end.  

- **Long Term Patterns** Observing the overall pattern for the CAD/JPY over the long term for this five year period it can be summarised as an overal downtrend. This is most prevalend early in the sample, with the last 4 years of the sample showing short term volatility but fairly flat. 

**Question:** Based on the p-value, is the model a good fit?

**Answer:** Based on the p-value this model does not appear to be a good fit. The p-value for Lag 2 is 0.140. Any p-value higher than 0.05 would be considered not significant. The p-value of Lag 1 as you can see is 0.00, this indicates a model using order=(1, 1) would be a better fit.

**Question:** What does the model forecast will happen to the Japanese Yen in the near term?

**Answer:** 
1. Based on the p-value this model does not appear to be a good fit. The p-value for all Lags 2 is > 0.05. Any p-value > than 0.05 would be considered not significant. 

2. The model forcasts a downward trend of Japanese Yen Price in the near term.

**Question:** What does the model forecast will happen to volatility in the near term?

**Answer:** The model forecasts **increased** volatility in the near term. 

# Conclusions

1. Based on your time series analysis, would you buy the yen now?
    * No, our modelling for returns was not a good fit, along with additional moddelling predicting an increase in volatility in the short term.

2. Is the risk of the yen expected to increase or decrease?
    * The volatility if the yen and therefore risk is expected to increase.

3. Based on the model evaluation, would you feel confident in using these models for trading?
    * No I wouldnt be confident trading with these models. Both the ARMA and ARIMA models where not a good fit for this data as evident from the p-values. The GARCH model was a better fit for the data, with the results showing us there would be an increase in volatility. I would not be confident trading on volatility predictions alone. 

4. Does this model perform better or worse on out-of-sample data as compared to in-sample data?
    * In general, a lower RMSE is better than a higher one. In conclusion the "out of sample" Test Data performed better then the "In Sample" Training Data. The difference between the two are Test Data (out of sample) RMSE = 0.6445820942663303 vs Training Data (in sample) MSE =  0.8418722775348019
