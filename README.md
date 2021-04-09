Here is a Python code for the paper "Inferring Mobility Measures from GPS Traces with Missing Data" by Ian Barnett and J.P. Onnela, following https://github.com/ianjamesbarnett/GPSimputation. 

All features are in features.py

## Python Dependencies
- Numpy
- Pandas
- Scipy
- Tqdm
- Scikit-learn

## Tutorial
1. Download demo data from [here](https://github.com/ianjamesbarnett/GPSimputation/tree/master/Tutorial/GPSExample.zip). This data contains a single user's daily GPS records.
2. Run the following command to write the extracted features to **output.tsv**

    > `main.py --input_dir GPSExample --output_file output.tsv`
 
3.  The rows of this file represent a single day in the range that the data set was collected over. Each column represents a different feature. The features are described here:
    1. Hometime:			Time spent at home (minutes)	
    2. DistTravelled:		Distance travelled (meters)
    3. RoG:				Radius of gyration (meters)
    4. MaxDiam:			Maximum diameter (longest distance between any two points) (meters)
    5. MaxHomeDist:		Maximum distance from home (meters)
    6. SigLocsVisited:	Number of significant locations visited that day
    7. AvgFlightLen:		Average length of flights on that day (meters)
    8. StdFlightLen:		Standard deviation of the length of flights on that day (meters)
    9. AvgFlightDur:		Average time flights took on that day (seconds)
    10. StdFlightDur:		Standard deviation of the time flights took on that day (seconds)
    11. ProbPause:			Probability (fraction of time) a person is stationary (paused) during a day (as opposed to mobile/in flight)
    12. SigLocEntropy:		Location entropy across a person's significant locations for the day.
    13. MinsMissing:		Number of minutes of missing data in a person's GPS mobility trace that day.
    14. CircdnRtn:			Circadian routine measuring similarity in a person's locations over the course of a day to that of the other days in the data set. Numeric between 0 and 1. 1=identical routine, 0=completely different routine.
    15. WkEndDayRtn:		Similar to the CircdnRtn measure, except comparisons are stratified by grouping together weekends and grouping together weekdays into two separate groups.

## Contact
* Shirley Hayati sahayati@upenn.edu
* Ian Barnett ibarnett@pennmedicine.upenn.edu
