# outliers
Detect Numerical Outliers | .conf2017

http://conf.splunk.com/files/2017/recordings/detect-numeric-outliers-advances.mp4


Splunk searches to detect numerical outliers in time series metrics!

I have uploaded a sample app that contains 2 simple dashboards depicting the timewrap and streamstats versions of the outlier searches. 

I recommend the timewrap version to get your feet wet with the concepts, then the streamstats for applying the approach to multiple series of data. 

You will need to edit the searches in the panels to create a timechart that makes sense in your environment. 

For example, in the timewrap panels, my search begins with:

`| tstats prestats=t count WHERE index=main by _time span=300s 
| timechart span=300s partial=f count `

Replace this with whatever timechart generating search makes sense for you!

I have also simply provided text files with the SPL for each method if you want to skip installing the sample app. 


KNOWN ISSUE : Timepicker on timewrap dash is not integrated into the searches, was working with fixed timeframe in the SPL, will open issue and fix when i have the chance. 
