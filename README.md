# The Endless Line Hackathon - README

## Project Overview

This repository contains the data and notebooks for the **The Endless Line Hackathon**, where participants are tasked with predicting waiting times at Euro-park, a global theme park. The goal is to leverage data science to improve visitor experience by accurately forecasting waiting times at key attractions, which in turn can help optimize the park's operations and KPIs.

## Challenge

Participants are required to:
- Model the waiting times at three key attractions in the park (Pirate Ship, Flying Coaster, Water Ride).
- Predict the waiting time 2 hours in advance, utilizing historical data and additional features such as weather conditions.
- Present their solution, including model development, data insights, and predictions, to a jury.

The main deliverables are:
1. A notebook with the code used to solve the problem.
2. Predictions tested on a hidden test set and compared to other teams using the leaderboard.

## Data

The following files are available for analysis:

1. **`waiting_times_train.csv`**: Historical waiting times for the three attractions with 15-minute granularity.
   - **WAIT_TIME_IN_2H**: The target variable representing the waiting time 2 hours ahead.
   - Other features: `Datetime`, `Entity_description_short`, `Adjust_capacity`, `Downtime`, `Current_wait_time`, `Time_to_parade_1`, `Time_to_parade_2`, and `Night_show`.

2. **`waiting_times_X_test_val.csv`**: Validation set to test your model (without the target variable).

3. **`weather.csv`**: Weather information at the park location, updated every 15 minutes.

## Model Development

Your task is to:
- Explore the structure and trends in the provided data.
- Develop a model to predict the waiting time 2 hours in advance using the training data.
- Test your model using the validation set.
- Make a final submission using the hidden test set for evaluation.

The chosen evaluation metric is the **Root Mean Squared Error (RMSE)**.

## Final Presentation

Each team will present their work in front of a jury:
- 5-minute pitch focusing on key components of your code.
- Conclusions on the data structure and trends, along with the final model used.
- A Q&A session with the jury.

Two winners will be announced:
1. Based on the leaderboard.
2. Based on the richness and creativity of the approach.

## Best Practices

- Structure your notebook and presentation.
- Focus on key insights and the most impactful parts of your solution.
- Split the work between team members to optimize time.
- Be honest about the challenges you encountered.

Good luck and enjoy the hackathon!
