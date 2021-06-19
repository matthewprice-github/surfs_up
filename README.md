# surfs_up

## Overview 
The purpose of this assignment was to gauge tempature trends in Oahu in order to better quantify market intest in a surf shop during the summer and winter months. 

## Results 
* We can see tempature summary statistics for the [June](https://github.com/matthewprice-github/surfs_up/blob/main/resources/June_temps.PNG) and [December](https://github.com/matthewprice-github/surfs_up/blob/main/resources/December_temps.PNG)
* In June, the average temp is ~75 degrees (F), with the minimum and maximum temps fluctuating between 64 degrees and 85 degrees, respectively. 
* In December the average temp is ~71 degrees (F), with the minimum and maximum temps fluctuating between 56 degrees and 83 degrees, respectively. 


## Summary 
Compared to the continental US, Oahu's tempertaures stay a lot more conistant between the seasons (staying nice all year around!). December occasionally hosts minimum temps that dip below prime surfing weather: seems like the bottom 1/4 of the temps are below 70 degrees. However, I would still say surfing prospects look promising for that month as a whole.  

One thing besides temperature that would be important to know for these months is precipitation, which thankfully we can also pull using the same methods we used for temperature. 

To pull all recorded precipitation data for June, we would use: 

```
date_str = "06"
June_prcp = session.query(Measurement.prcp).filter(func.strftime("%m", Measurement.date) == date_str).all()
```
To pull the same data for December, we simply have to adjust the date string 

```
date_str = "12"
Dec_prcp = session.query(Measurement.prcp).filter(func.strftime("%m", Measurement.date) == date_str).all()
```

This way we can look at the frequency of rain, which would impact peoples interest in surfing. 
