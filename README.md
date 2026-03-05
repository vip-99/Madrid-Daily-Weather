# Madrid-Daily-Weather

## Madrid Weather Analysis Dashboard (1997–2015)


## Project Objective

The objective of this project is to analyze daily weather conditions in Madrid from 1997 to 2015 and identify climate patterns, seasonal variations, and weather trends.
The analysis focuses on key meteorological variables such as maximum, minimum, and mean temperature, humidity, wind speed, visibility, pressure, dew point, precipitation events, cloud cover, and wind direction.






## Using data visualization and analytical techniques, the project aims to


1. Understand temperature fluctuations and seasonal patterns

2. Examine the relationship between humidity and atmospheric pressure

3. Analyze wind speed and cloud cover variations

4. Identify the distribution of weather events such as rain, fog, and thunderstorms

5. Provide an interactive dashboard for better weather trend exploration.



## Tools Used

1. Power BI Desktop – Data visualization and dashboard creation

2. Power Query – Data cleaning and transformation

3. DAX (Data Analysis Expressions) – Creating calculated measures and KPIs

4. Excel / CSV Dataset – Source data for weather records



## Key DAX Measures Used

Average Maximum Temperature
```
Avg Max Temp = AVERAGE(Weather[Max_TemperatureC])
```

Average Humidity
```
Avg Humidity = AVERAGE(Weather[Humidity])
```

Average Wind Speed
```
Avg Wind Speed = AVERAGE(Weather[Wind_SpeedKm_h])
```

Average Pressure
```
Avg Pressure = AVERAGE(Weather[Sea_Level_PressurehPa])
```

Rain Days
```
Rain Days =
CALCULATE(
    COUNTROWS(Weather),
    Weather[Events] = "Rain"
)
```

Days of Data (Based on Selected Date Range)
```
Days of Data =
DATEDIFF(
    MIN('Date'[Date]),
    MAX('Date'[Date]),
    DAY
)
```


## Key Insights
1. Clear Weather Dominates Madrid
```
The analysis shows that clear weather conditions occur nearly 80% of the time, indicating that Madrid experiences predominantly stable and sunny weather throughout the year. Rain, fog, and thunderstorms make up a relatively small percentage of weather events.
```

2. Moderate Temperature Variations
```
The dashboard indicates an average maximum temperature of around 25–26°C, while minimum temperatures remain significantly lower. This reflects moderate seasonal temperature variations typical of a Mediterranean climate.
```

3. Humidity and Pressure Relationship
```
The humidity and sea-level pressure visualization reveals that humidity fluctuates moderately while pressure remains relatively stable around 1019 hPa, indicating consistent atmospheric pressure conditions in Madrid.
```

4. Wind Speed Patterns
```
The mean wind speed analysis shows most days experience moderate wind speeds between 5–12 km/h, suggesting calm weather conditions are common.
```

5. Limited Rainfall Occurrence
```
The dataset indicates approximately 45 rainy days in the selected period, meaning precipitation events are infrequent compared to clear weather conditions.
```

6. Cloud Cover Variability
```
Cloud cover analysis shows periodic increases during certain days, often associated with rain or fog events, while most days have low cloud coverage.
```


## Dashboard Features

***Temperature trend analysis (Max, Min, Mean)***

***Humidity vs Sea-Level Pressure comparison***

***Weather event distribution visualization***

***Wind speed pattern analysis***

***Cloud cover trends***

***Interactive date and month filtering***

***Summary KPIs for quick insights***
