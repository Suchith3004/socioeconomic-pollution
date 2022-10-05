
# Air Quality Prediction in Urban Settings: Based on Socioeconomic Status

CS5834 - Intro to Urban Computing (Fall 2021)

With the extensive parallel development of urban areas and rise in global warming greater attention has been directed towards environment protection and studying the relationships between the two.\cite{urbansprawl} Air quality in the United States is improving on average as the time goes by.[[1](https://usafacts.org/earth-day-facts/spotlight-air-quality/?utm_source=google&utm_medium=cpc&utm_campaign=ND-SOTE21&gclid=CjwKCAiA-9uNBhBTEiwAN3IlNNWjmRKbknHLBBlBwpJ7eIXB1rJvHm4wSlM4T-6nfSjZR34-AGX7-hoCRUIQAvD_BwE)] However, the improvement of air quality is not equally distributed over all regions of the U.S. For one, air quality is expected to be worse in more populated areas. So, we further explore such variables, specifically socioeconomic status, for its potential to be an indicator of air quality. We 1) examine the Pearson correlation and 2) attempt to use traditional ML classification models to predict air pollution levels using socioeconomic status data from 2005-2019 across 339 metropolitan areas in the United States. The results of cross-correlation showed a moderate relationship and the classification models did not score high enough to conclude that there is a strong relationship between socioeconomic status and air pollution. More specifically, we collected a comprehensive social economics dataset including income, education, occupation [[2](https://www.apa.org/pi/ses/resources/class/measuring-status)] information from over 300 cities in the U.S. during 2005 to 2016 and an air quality dataset with all concentrations of major air pollution matter(Pm2.5, Sulfur Dioxide, etc) for each year. To study the correlation between socio-economic status and air pollution, we first performed an un-supervised clustering on the air pollution dataset, generating a cluster label for each instance. This cluster label can be regarded as a straightforward evaluation of air pollution level, because we have over 5 air pollution metrics. Then we further developed two models: Long-short term memory(LSTM) and multinomial Logistic regression model(MLRM) using social economics data as input and predict their cluster label. If our models can predict air quality cluster labels with high accuracy, we can say that social economic status is strong indicator of air quality. The results of cross-correlation showed a moderate relationship and the classification models did not score high enough to conclude that there is a strong relationship between socioeconomic status and air pollution. We concluded that a larger time range must be studied at a more granular level to declare with confidence the nature of the relationship between the features and targets.
## Tech Stack

This project was primarily implmented in the Jupyter Lab enviornment. 

Python Libraries: PyTorch, Scikit-Learn, Transformers, SciPy

## Run Locally

Clone the project

```bash
  git clone https://github.com/Suchith3004/socioeconomic-pollution.git
```

Go to the project directory

```bash
  cd socioeconomic-pollution
```

Install dependencies

```bash
  pip install -r requirements.txt
```

Retrieve a EPA API Key

```bash
  curl curl https://aqs.epa.gov/data/api/signup?email=myemail@example.com
```

Create a file for EPA API Credentials

```bash
  touch epa_credentials.txt
```

Add the API Credentials in the following format

```text
email=myemail@example.com
key=123456
```


## Dataset

The AQI Report dataset was scraped from https://www.epa.gov/outdoor-air-quality-data/air-quality-index-report using a Selenium script. 

The US Census data is accesible at https://www.census.gov/data/developers/data-sets/acs-1year.2019.html.
## Authors

- Suchith Suddala - [@suchith3004](https://www.github.com/suchith3004)
- Juwon Park - [@juwon2239](https://github.com/juwon2239)
- Lihui Zhang - [@seraphD](https://github.com/seraphD)