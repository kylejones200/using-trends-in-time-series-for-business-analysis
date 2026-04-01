# Using Trends in Time Series for Business Analysis In this post we look at parametric and nonparametric methods for
identifying trends in time series data. It covers techniques like
least...

### Using Trends in Time Series for Business Analysis
In this post we look at parametric and nonparametric methods for
identifying trends in time series data. It covers techniques like least
squares estimation and differencing, highlighting how the choice of
trend identification method can impact forecasting.


<figcaption>Photo by <a
class="markup--anchor markup--figure-anchor"
rel="photo-creator noopener" target="_blank">Jonatan Pie</a> on <a
class="markup--anchor markup--figure-anchor"


#### Parametric Trend
When analyzing time series data, one of the first steps is to identify
any underlying trends. A parametric approach to trend identification
involves fitting a predetermined model or function to the data. The most
common parametric method is linear regression, where a straight line is
fit to the data using the method of least squares. This approach assumes
that the time series can be described by an equation:


where y_t is the observed value at time t, a is the intercept, b is the
slope (representing the trend), and e_t is the error term. The least
squares estimation procedure finds the values of a and b that minimize
the sum of the squared differences between the observed values and the
fitted line.

Parametric methods like linear regression make the assumption that the
data will revert to the mean over time. This means that deviations from
the trend line are temporary, and the series will eventually converge
back to the underlying trend. While this can be a reasonable assumption
in many cases, it may not hold true if there are significant structural
changes or persistent shocks to the system.

#### Nonparametric Methods
Instead of parametric trend analysis, we can use nonparametric
techniques which do not rely on fitting a predetermined (linear) model
to the data. Instead, these methods aim to identify trends in a more
flexible and data-driven way.

One popular nonparametric approach is the use of moving averages. In
this method, the trend is estimated by calculating the average of the
previous k observations, where k is the window size of the moving
average. This can help to smooth out short-term fluctuations and reveal
the underlying trend. The choice of window size is crucial, as a smaller
window will be more responsive to recent changes, while a larger window
will produce a smoother trend line.

Another nonparametric technique is the use of the median rather than the
mean. The median is less sensitive to outliers and extreme values than
the mean, which can be heavily influenced by these observations. This
can be particularly useful when the time series exhibits occasional
spikes or unusual events that do not represent the true underlying
trend.

Nonparametric methods help when the data does not conform to the
assumptions of parametric models, such as linearity or stationarity.
They can also be more robust to structural breaks or changes in the
data-generating process over time. However, nonparametric approaches may
be less efficient than parametric methods when the underlying
assumptions are met and they can be more computationally intensive.

Nonparametric methods can be more flexible in adapting to changes in the
trend. Moving averages, for example, can quickly adjust to shifts in the
underlying trend, as the trend estimate is based on the most recent
observations. This can make nonparametric approaches more suitable for
forecasting in the presence of structural breaks or other changes in the
data-generating process.

Additionally, the sensitivity of the trend estimate to outliers can also
impact forecasting. If the time series contains significant outliers or
unusual events, a parametric approach that is heavily influenced by
these observations may produce less reliable forecasts. In such cases, a
nonparametric method that is more robust to outliers, such as the
median-based trend, may be preferable.

#### Advantages and disadvantages of parametric and nonparametric methods
**Parametric Trend Analysis**

Advantages: Parametric models require the estimation of a relatively
small number of parameters, which can make them computationally
efficient and easier to interpret (aka Parsimonious models). Parametric
models can be used to extrapolate the trend beyond the observed data,
allowing for forecasting. Parametric methods make it easy to calculate
inference values.

Disadvantages: Parametric methods assume the data is independent and
identically distributed (which is not true for time series). The
mean-based estimation used in parametric methods can be heavily
influenced by outliers or extreme observations, leading to distorted
trend estimates.

**Nonparametric Trend Analysis**

Advantages: Nonparametric methods are more flexible and do not impose a
predetermined functional form on the trend. Nonparametric approaches are
more resistant to the influence of outliers and extreme values.
Nonparametric methods generally require fewer assumptions about the
underlying data-generating process, making them more widely applicable.

Disadvantages: Nonparametric methods can be less intuitive and harder to
interpret than parametric models, as they do not provide a clear
mathematical representation of the trend. Nonparametric approaches (like
moving averages) may not be as well-suited for extrapolating the trend
beyond the observed data, limiting their usefulness for forecasting.
Nonparametric methods can be more computationally intensive, especially
for large datasets or complex trend patterns.

In real life, the choice between parametric and nonparametric trend
analysis depends on the specific characteristics of the time series, the
objectives of the analysis, and the tradeoffs between accuracy,
interpretability, and computational requirements.

#### Reflection Question
**How can different trend identification methods impact forecasting?**
The choice of trend identification method can have significant
implications for forecasting future values of the time series.
Parametric methods, such as linear regression, rely on the assumption
that the trend will continue in a linear fashion. This may work well if
the underlying trend is indeed linear and stable over time. However, if
the trend exhibits nonlinearities or structural changes, parametric
models may struggle to capture these dynamics, leading to biased or
inaccurate forecasts.

### Related Stories
- [[ARIMA Models and Time Series Forecasting for Business
  Analytics](https://medium.com/@kylejones_47003/arima-models-and-time-series-forecasting-for-business-analytics-97c5c870e9c6)]
- [[Time Series Forecast Evaluation for Business
  Analytics](https://medium.com/@kylejones_47003/time-series-forecast-evaluation-for-business-analytics-3f5b6a634717)]
- [[What is a Time Series? An introduction for business
  analysts](https://medium.com/@kylejones_47003/what-is-a-time-series-an-introduction-for-business-analysts-303e8e1fedd8)]
