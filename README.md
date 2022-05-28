# Memphis-Police-911-Calls

The Memphis Police Department and their dispatchers have a goal of trying to answer 95% of all calls, within 20 seconds of them seizing the Public Safety Answering Point (PSAP). I set out to try to find, given a certain amount of working dispatchers and expected monthly calls, how many calls needed to be answered every hour to achieve this goal.

The data provided was found on the Memphis Data Hub (https://data.memphistn.gov/Public-Safety/911-Performance/sfvz-ctaq). This dataset tracks 911 call volume, percent answered within 20 seconds, percent of calls abandoned (hung up before being answered), and total wait time for caller (sum of dispatcher setup time, caller queue time, and ring time). These metrics allow for analysis to provide insight on call volume trends and how efficient dispatchers are by measuring historical total wait times for callers. 

The function used to find the optimal number of calls answered per hour to acheive the 95% answer rate was:
  
  _(((((x * .95) / 30.5) * (z+t)) / 60) / 24) / a
  
  _where x = call volume, z = average call length, t = total wait time, a = number of dispatchers working for a given hour
  

I created an excel dashboard to provide an overview of the Memphis Police Deparment dispatchers and how successful they have been in reaching their goals. You can download the workbook where there are chart sliders that show how call length and number of dispatchers on duty, have varying degrees of magnitude on the amount of calls needed by each dispatcher. I have also provided a .png of the dashboard itself, in case you didn't want to download the excel file.  
