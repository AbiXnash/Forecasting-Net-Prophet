# Forecasting-Net-Prophet

Time-series analysis and forecasting with [Prophet](https://facebook.github.io/prophet/), written as a growth analyst
at MercadoLibre. One Google Colab notebook answers four questions:

1. **Unusual patterns:** was Google search traffic for the company unusual in May 2020, the month of its quarterly
   results? (Compares May's total with the monthly median.)
2. **Seasonality:** how does search traffic vary by hour of day, day of week and week of year? (hvPlot charts and
   a heatmap.)
3. **Search vs. stock price:** does lagged search traffic relate to stock volatility or hourly returns? (Adds
   `Lagged Search Trends`, `Stock Volatility` and `Hourly Stock Return` columns and a correlation table.)
4. **Forecasts:** a Prophet model of hourly search traffic about 80 days ahead, with its trend and seasonal
   components, and a Prophet forecast of daily revenue for the next quarter, with a total for the finance team.

## Data

The notebook uploads three CSVs in Colab: `google_hourly_search_trends.csv`, `mercado_stock_price.csv` and
`mercado_daily_revenue.csv`. They aren't included in this repository.

## Run it

Open `forecasting_net_prophet.ipynb` in [Google Colab](https://colab.research.google.com/) and run the cells. The
first cell installs `pystan`, `fbprophet`, `hvplot` and `holoviews`. The `fbprophet` package has since been renamed
`prophet`; on a current Python, install `prophet` and change the import to `from prophet import Prophet`.

## Licence

MIT, see [LICENSE](LICENSE).
