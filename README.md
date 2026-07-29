# Industrial Energy Analysis

I used a real industrial energy dataset to practise cleaning time-series data,
exploring it with pandas and Matplotlib, and building a basic regression model.

The notebook predicts the next 15 minutes of electricity use from recent meter
readings and calendar features. I compare linear regression and random forest
against a last-reading baseline, then evaluate them with MAE, RMSE and R2.

The data comes from a small steel facility in South Korea. I chose it because
the same type of workflow could be used with manufacturing data from a paper
mill or corrugated packaging plant.

Dataset: [Steel Industry Energy Consumption, UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/851/steel+industry+energy+con)

## Run it

```bash
pip install -r requirements.txt
jupyter notebook industrial_energy_analytics.ipynb
```

The notebook downloads the data automatically the first time it runs.

## Findings

- Electricity use changes noticeably by hour and between working and non-working days.
- Random forest had the lowest RMSE at 10.91 kWh and the highest R2 at 0.879.
- The last-reading baseline had a slightly lower MAE than random forest, showing that a simple baseline can still be competitive.
