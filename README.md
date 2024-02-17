This is a repository meant to facilitate our collaboration during a hackathon supervised by eleven-strategy data scientists.
The main goal of the hackathon is to compete to predict the waiting after two hours in some attractions in an amusement park. The details are provided in the file pdf 'onboard'.
The data at disposition are the waiting_times_test (and validation) files which includes logistic data and another file, "weather", which includes meteorological data.


0) Preprocessing

  The first difficulty is to use efficiently the data at disposition. We distinguished two main problems. First we must interpret the meaning of the lacking data in rain_1h snow_1h and in time_to_parade.
  One should give a coherent value according to the approach chosen for those lacking values. The second one is the choice of the approach. The waiting_time in two hours looks particularly linked to the
  current waiting time. This relation looks proportionnal after visualisation. However, it is not the case for any of the other value. One month may contains a period of holidays which leads to more visits
  than the consecutive month. We may think that the time_to_parade data may have an impact when the show is close to the time studied. Finally what to do with the weather dataset ?

We focused on three main approaches:

1) Classification:

  We noticed that the waiting time was always between 0 and 90 minutes and always a multiple of five. Since our predictions must be accurate with a tolerance of five minutes, we decided to split the time into 90/5=18
  intervals of five minutes.
  After a OneHotEncoding of those class we arrive at a first satisfying result. We achieve a loss of 11,21 (RMSE) on the validation set with a RandomForest training.

2) Logistic Regression

   We chose at this point to simplify the input data. For instance, we stopped using the weather dataset. We stopped using the season but only the months. However, we found on the litterature that in such,
   cases we could use a cosinus function to insinuate the periodicity of temporal data. For exemple the output of 31 must be close to the output of 1 since the two days may be consecutive. This way we insist
   on the similarity between two consecutive days. We howerver make a distinction between workdays and sunday and saturday for our model.
   Finally we found better results after using an xgboost regressor with a loss value of 9,01 on the dataset.

 3) Others

  Many other approches and neaural networks method were tested which can be found in the "hackathon_arnaud" file
